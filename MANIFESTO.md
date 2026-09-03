# Manifeste Platform Engineering
### Séance d'ouverture — Projet fil rouge Dev/Ops, DIIAGE

Ce manifeste s'inspire de trois sources reconnues du domaine — le *CNCF Platforms White Paper*, l'approche *Platform as a Product* popularisée par la communauté Team Topologies / Humanitec, et les principes de golden path du mouvement platform engineering — reformulées et adaptées au contexte spécifique de ce projet : plateforme Kubernetes on-premise,

Il ne remplace pas les ADR. Il donne le cadre dans lequel elles se jugent.

---

## Les dix principes

**1. Une plateforme est un produit, pas un projet.**
Elle a des utilisateurs, pas des bénéficiaires. Elle s'arrête quand ils cessent de l'utiliser, pas quand vous cessez de la construire.

**2. Vous ne détenez pas de droit de passage.**
Une équipe produit peut toujours faire sans vous — plus lentement, moins bien outillée, mais elle peut. Le jour où votre plateforme devient obligatoire, elle a cessé d'être un service.

**3. Le chemin goudronné est optionnel, plus rapide, et sa sortie est documentée.**
Retirez une de ces trois propriétés et vous avez un mur, pas un chemin.

**4. Retirer de la charge, jamais la déplacer ni l'ajouter.**
Une abstraction qu'il faut comprendre en plus de ce qu'elle abstrait n'est pas une plateforme — c'est une dette supplémentaire, déguisée en service.

**5. Le self-service est l'objectif ; la collaboration a une date de fin.**
Rester en mode collaboration parce que c'est gratifiant, sans jamais produire l'abstraction qui le rendrait inutile, est un échec de conception — pas un signe d'engagement.

**6. Un contournement n'est pas de l'indiscipline. C'est votre meilleur capteur.**
Si une équipe vous contourne, votre chemin était plus lent que son besoin. Reprochez le contournement une fois, et il ne sera plus jamais signalé.

**7. L'organisation produit l'architecture — la loi de Conway ne se négocie pas.**
Deux sous-groupes qui ne se parlent pas produiront deux composants qui ne s'intègrent pas, quels que soient vos diagrammes.

**8. Une décision se défend, elle ne se justifie pas.**
Défendre, c'est énoncer à l'avance la condition qui vous ferait changer d'avis. Justifier, c'est chercher cette condition après coup, en connaissant déjà le résultat.

**9. Un contrôle non-bloquant est une checklist, pas une garde-fou.**
Un scanner que personne ne fait respecter n'est pas une mesure de sécurité relâchée — c'est l'absence de mesure, avec un tableau de bord en plus.

**10. Le meilleur indicateur de votre réussite est le moment où on cesse d'avoir besoin de vous parler.**
Pas un chiffre sur un dashboard. Le silence des sollicitations manuelles.

---

## Pourquoi ça compte encore, à l'ère de l'IA

Générer du code sur mesure n'a jamais été aussi rapide. Un développeur peut aujourd'hui produire seul, en une session de travail, ce qui prenait une équipe : un pipeline, un tableau de bord, le scaffolding d'une API.

Ça ne change rien à ce que ce manifeste protège. L'IA réduit le coût de construire ; elle ne réduit pas le coût de tenir en production, patcher, sécuriser, comprendre trois ans plus tard ce qu'une autre équipe a généré sans jamais documenter pourquoi. La loi de Conway (principe 7) ne se négocie pas avec un modèle de langage : des équipes qui ne se parlent pas produiront N variantes du même problème, plus vite qu'avant, pas moins.

Une plateforme n'est plus en concurrence avec « je peux le coder moi-même ». Elle décide quelle part de ce que chacun peut désormais générer devient un chemin partagé, maintenu et compris — plutôt qu'un énième artefact que son auteur est seul à savoir faire fonctionner.

---

## Ce que ce manifeste ne dit pas

Il ne dit pas quels outils utiliser — c'est votre décision, à défendre par ADR.
Il ne dit pas comment vous organiser en interne — la structure des squads et de la rotation transverse est donnée, le reste (rôles, rituels, arbitrages) reste à vous.
Il ne dit pas ce qui est *vrai en général* en platform engineering — il dit ce que ce cours a choisi de retenir, et pourquoi.

---

*Inspiré du CNCF Platforms White Paper (TAG App Delivery), de l'approche Platform as a Product (communauté Team Topologies / Humanitec), et des principes de golden path popularisés par PlatformCon — reformulés pour ce projet, pas reproduits.*
