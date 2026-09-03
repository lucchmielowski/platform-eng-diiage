# RFC-003 : Comment le service Notifications doit-il accéder aux données du service Compte ?

**Statut :** Clôturée [ADR-001](./adr.md)
**Auteur :** Équipe Notifications
**Ouverte le :** 2026-08-18
**Clôture :** 2026-08-25

## Question précise

Le service Notifications a besoin de lire des informations de profil (email, préférences de contact) détenues par le service Compte pour envoyer ses notifications. Faut-il lui donner un accès direct à la base du service Compte, ou construire un mécanisme de duplication contrôlée ?
  
Ce n'est pas encore une décision : c'est une question ouverte, soumise avant qu'un choix soit tranché. L'objectif de cette RFC est de vérifier qu'aucun scénario d'échec n'a été oublié avant de trancher.

## Contexte

Le service Notifications consulte aujourd'hui, ponctuellement et via un script manuel, la base du service Compte pour récupérer les emails à jour. Cette pratique doit être remplacée par une intégration propre avant l'ouverture du service à un second canal (SMS), qui multipliera la fréquence de ces lectures.

## Options envisagées

**Option A: Accès direct en lecture à la base du service Compte.**
Le plus rapide à mettre en œuvre. Pas de synchronisation à construire.

**Option B: Duplication contrôlée via un contrat explicite.**
Le service Compte publie les changements de profil pertinents (événement ou API dédiée) ; le service Notifications en conserve une copie locale, réconciliée périodiquement.

**Option C: Appel synchrone à la demande, sans copie locale.**
Le service Notifications interroge une API du service Compte à chaque envoi, sans rien stocker localement.

## Proposition technique : mécanisme de réconciliation (Option B)

Esquisse volontairement partielle, jointe pour donner aux relecteurs quelque chose de concret à contester plutôt qu'un principe abstrait. Elle n'est pas figée : voir « Points ouverts » ci-dessous.

**Flux nominal — événement.**
Le service Compte publie un événement à chaque changement de profil pertinent pour Notifications.

```json
// topic: compte.profil.mis_a_jour
{
  "compte_id": "cus_9f2a1e",
  "email": "utilisateur@example.com",
  "preferences_contact": { "email": true, "sms": false },
  "version": 42,
  "mis_a_jour_le": "2026-08-20T09:14:00Z"
}
```

Le service Notifications consomme cet événement et met à jour sa copie locale (`profils_notifications`) si `version` est strictement supérieur à la version déjà stockée pour ce `compte_id` — un événement reçu dans le désordre ou en double est ignoré sans erreur.

**Filet de sécurité — réconciliation périodique.**
Les événements peuvent être perdus (panne du bus, redémarrage sans replay). Un job planifié compense la dérive plutôt que de supposer une livraison fiable :

| | |
|---|---|
| `GET /internal/comptes/profils` | Export paginé des profils, côté service Compte |
| Paramètres | `mis_a_jour_depuis` (ISO 8601), `curseur`, `limite` (défaut 200) |
| Réponse | `{ "profils": [...], "curseur_suivant": "..." }`, même forme que l'événement |
| Fréquence | Toutes les 6h sur la fenêtre glissante des 48h précédentes |
| Sur écart détecté | La valeur du service Compte fait autorité ; écart et `compte_id` loggués pour audit |

**Points ouverts (non tranchés par cette RFC).**

- Fréquence de réconciliation : 6h est un point de départ, pas une valeur défendue. À confirmer selon le volume réel une fois le canal SMS ouvert.
- Ce que fait Notifications d'un profil réconcilié en écart alors qu'une notification est déjà en file avec l'ancienne valeur — rejouer, ignorer, ou best-effort ?
- Qui est propriétaire du schéma de l'événement (`compte.profil.mis_a_jour`) une fois publié : versionnement, dépréciation des champs.

## Ce qui est demandé aux relecteurs

- Un scénario d'échec ou de charge que ces options n'auraient pas anticipé.
- Une objection sur le coût de maintenance de l'option B côté service Compte (contrat à faire évoluer avec gestion de compatibilité).
- Une date de disponibilité pour trancher : la clôture est fixée au 2026-08-25, au-delà de laquelle l'absence de retour vaut silence, pas véto.

## Résumé des retours (par l'auteur)

- **Équipe Compte :** l'option A est refusée du côté propriétaire. Un accès direct empêcherait toute restauration ciblée de leur base sans risquer de casser Notifications silencieusement. Confirme être prête à maintenir un contrat d'exposition (option B) si son périmètre reste limité aux champs réellement consommés.
- **Équipe Plateforme :** signale que l'option C introduit une dépendance de disponibilité (Notifications tombe si Compte tombe), ce qui est jugé inacceptable pour un canal utilisateur critique.
- **Équipe Notifications (auteur) :** convergence vers l'option B. Un point non résolu: la conception du mécanisme de réconciliation en cas de dérive devra être revu plutôt que bloqué .

## Décision consécutive

Cette RFC n'a pas tranché : elle a réduit trois options à une, et fait remonter une contrainte (le refus de l'option A côté propriétaire) qui n'était pas visible au départ. La décision elle-même, avec ses alternatives écartées et son signal de révision, est actée dans [ADR-001](./adr.md).
