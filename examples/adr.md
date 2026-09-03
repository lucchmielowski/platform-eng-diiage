# ADR-001 : Duplication contrôlée plutôt qu'accès direct à la base entre services

**Statut :** Acceptée
**Date :** 2026-09-03
**Décideurs :** Équipe plateforme, en concertation avec les deux équipes produit concernées

## Contexte

Deux services demandent un accès direct à la même base pour éviter une duplication de données. Le besoin métier : les deux services consomment en partie les mêmes informations, et maintenir deux copies introduit un risque de désynchronisation. La solution la plus rapide à court terme serait d'ouvrir un accès direct du second service à la base du premier.

Cet accès casserait cependant l'isolation entre services : plus aucune restauration, migration ou changement de schéma ne pourrait se faire côté propriétaire sans risquer de casser le consommateur, silencieusement et à distance.

## Décision

Chaque service garde sa propre base. La duplication contrôlée remplace l'accès direct : le service propriétaire expose les données nécessaires via un contrat explicite (événement ou API), et le second service en conserve une copie locale, synchronisée par ce contrat plutôt que par une lecture directe en base.

## Alternatives écartées

**Base partagée entre les deux services.**
Plus simple à court terme, pas de synchronisation à construire, pas de latence de propagation. Rejetée pour ce système, pas dans l'absolu : elle interdit toute restauration ciblée (un rollback du propriétaire embarque de fait le consommateur) et couple les deux équipes sur chaque migration de schéma, y compris sur des colonnes que le consommateur n'utilise pas.

**Appel synchrone à la demande (API interne) sans copie locale.**
Évite la duplication complètement. Rejetée pour ce système : le second service devient indisponible dès que le premier l'est, ce qui transforme une dépendance de données en dépendance de disponibilité.

## Signal de révision

Si la duplication cause une dérive de données que la réconciliation ne résout plus, comme des écarts récurrents entre la copie et la source que le mécanisme de synchronisation ne rattrape pas dans un délai raisonnable, la décision est rouverte.

## Conséquences

- Le service consommateur doit implémenter et maintenir un mécanisme de réconciliation, pas seulement une réception d'événements.
- Le service propriétaire doit traiter son contrat d'exposition (événement/API) comme une interface publique
- Le couplage entre les deux équipes se déplace de la base de données vers le contrat plus explicite.
