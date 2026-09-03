---
marp: true
theme: diiage
paginate: true
inlineSvg: true
size: 16:9
html: true
style: |
  section {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Helvetica Neue', Arial, sans-serif;
    background: #ffffff;
    color: #1a1a2e;
    padding: 60px 70px;
    font-size: 25px;
    line-height: 1.5;
  }

  section.title {
    background: #14142b;
    color: #ffffff;
    justify-content: center;
  }
  section.title h1 {
    font-size: 2.6em;
    font-weight: 800;
    margin-bottom: 0.15em;
    border: none;
    color: #ffffff !important;
  }
  section.title h2 {
    font-size: 1.1em;
    font-weight: 400;
    color: #9a9ab8;
    border: none;
    text-transform: none;
    letter-spacing: normal;
    margin: 0;
  }
  section.title li {
    color: #d8d8ec;
    font-size: 0.85em;
    margin-top: 1.2em;
  }
  section.title li::marker {
    color: #7a7aff;
  }

  section.closing {
    background: #14142b;
    color: #ffffff;
  }
  section.closing h2 {
    color: #ffffff;
    border-bottom: 2px solid #4a4a7a;
    padding-bottom: 0.3em;
  }
  section.closing li {
    color: #e4e4f0;
  }
  section.closing li::marker {
    color: #7a7aff;
  }

  section.section {
    background: #14142b;
    color: #ffffff;
    justify-content: center;
  }
  section.section .section-num {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    width: 48px;
    height: 48px;
    border-radius: 50%;
    background: #7a7aff;
    color: #ffffff;
    font-weight: 800;
    font-size: 0.9em;
    margin-bottom: 0.7em;
  }
  section.section h1 {
    font-size: 2.7em;
    font-weight: 800;
    margin: 0 0 0.3em 0;
    border: none;
    color: #ffffff !important;
  }
  section.section p.subtitle {
    font-size: 1.05em;
    color: #9a9ab8;
    margin: 0;
    font-weight: 400;
  }

  p.eyebrow {
    font-size: 0.62em;
    font-weight: 700;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: #6a6aa0;
    margin: 0 0 0.2em 0;
  }

  h2 {
    font-size: 1.5em;
    font-weight: 800;
    color: #14142b;
    margin: 0 0 0.5em 0;
    letter-spacing: -0.01em;
    border: none;
  }

  ul {
    margin-top: 0.3em;
  }
  li {
    margin-bottom: 0.35em;
    color: #2a2a40;
  }
  li::marker {
    color: #7a7aff;
    font-weight: 700;
  }

  table {
    font-size: 0.68em;
    border-collapse: collapse;
    width: 100%;
  }
  table th {
    background: #14142b;
    color: #ffffff;
    font-weight: 700;
    padding: 0.5em 0.7em;
    text-align: left;
  }
  table td {
    padding: 0.5em 0.7em;
    border-bottom: 1px solid #e4e4f0;
  }
  table tr:nth-child(even) td {
    background: #f7f7fc;
  }

  .timeline {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-top: 2.5em;
    padding: 0 1em;
    position: relative;
  }
  .timeline::before {
    content: '';
    position: absolute;
    top: 17px;
    left: 6%;
    right: 6%;
    height: 3px;
    background: #e4e4f0;
  }
  .timeline-node {
    flex: 1;
    text-align: center;
    position: relative;
    z-index: 1;
  }
  .timeline-dot {
    width: 34px;
    height: 34px;
    border-radius: 50%;
    background: #6a6aa0;
    color: #ffffff;
    display: flex;
    align-items: center;
    justify-content: center;
    font-weight: 800;
    font-size: 0.75em;
    margin: 0 auto 0.7em;
  }
  .timeline-dot.accent {
    background: #e8505b;
    box-shadow: 0 0 0 5px #fbe4e5;
  }
  .timeline-dot.wide {
    width: auto;
    height: auto;
    min-width: 34px;
    padding: 9px 18px;
    border-radius: 20px;
    font-size: 0.8em;
    white-space: nowrap;
  }
  .timeline-label {
    font-weight: 700;
    font-size: 0.8em;
    color: #14142b;
  }
  .timeline-desc {
    font-size: 0.65em;
    color: #6a6a90;
    margin-top: 0.3em;
  }

  .quad {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 16px;
    margin-top: 1.3em;
  }
  .quad-card {
    background: #f7f7fc;
    border-radius: 10px;
    padding: 18px 20px;
  }
  .quad-card h4 {
    margin: 0 0 8px 0;
    font-size: 0.75em;
    font-weight: 800;
    color: #6a6aa0;
    text-transform: uppercase;
    letter-spacing: 0.07em;
  }
  .quad-card p {
    margin: 0;
    font-size: 0.78em;
    color: #2a2a40;
    line-height: 1.4;
  }

  .trio {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
    margin-top: 1.3em;
  }
  .trio .quad-card p {
    font-size: 0.68em;
  }

  .chip-row {
    display: flex;
    gap: 12px;
    margin-top: 1.4em;
    width: 100%;
  }
  .chip {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    background: #14142b;
    color: #ffffff;
    padding: 18px 14px;
    border-radius: 14px;
    font-size: 0.85em;
    font-weight: 800;
  }

  .diagram {
    margin-top: 1em;
  }
  .diagram svg,
  .diagram img {
    display: block;
    margin: 0 auto;
  }

  .decision {
    display: flex;
    gap: 28px;
    margin-top: 1.3em;
    align-items: flex-start;
  }
  .checklist {
    flex: 1.1;
  }
  .check-item {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 0.78em;
    margin-bottom: 12px;
    color: #2a2a40;
  }
  .check-num {
    width: 22px;
    height: 22px;
    border-radius: 50%;
    background: #e4e4f0;
    color: #6a6aa0;
    font-weight: 800;
    font-size: 0.75em;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
  }
  .verdicts {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 12px;
  }
  .verdict {
    border-radius: 10px;
    padding: 14px 18px;
  }
  .verdict.low {
    background: #f7f7fc;
    border: 1.5px dashed #c8c8e0;
  }
  .verdict.high {
    background: #eef0ff;
    border: 1.5px solid #7a7aff;
  }
  .verdict-label {
    font-size: 0.62em;
    font-weight: 800;
    text-transform: uppercase;
    letter-spacing: 0.06em;
    color: #6a6aa0;
    margin-bottom: 4px;
  }
  .verdict-value {
    font-size: 0.8em;
    font-weight: 700;
    color: #14142b;
  }

  .timeline-desc .ok {
    color: #2f9e5c;
    font-weight: 700;
  }
  .timeline-desc .bad {
    color: #e8505b;
    font-weight: 700;
  }

  .badge {
    display: inline-block;
    padding: 4px 10px;
    border-radius: 12px;
    font-size: 0.62em;
    font-weight: 800;
    text-transform: uppercase;
    letter-spacing: 0.03em;
    margin-top: 10px;
  }
  .badge.good {
    background: #e3f5ea;
    color: #2f9e5c;
  }
  .badge.bad {
    background: #fbe4e5;
    color: #e8505b;
  }
  .badge.moved {
    background: #fdf0dc;
    color: #c9821a;
  }

  .example-tag {
    display: inline-block;
    background: #fbe4e5;
    color: #c23a44;
    font-size: 0.6em;
    font-weight: 800;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    padding: 5px 12px;
    border-radius: 6px;
    margin-bottom: 0.7em;
  }

  strong {
    color: #14142b;
    font-weight: 800;
  }

  section::after {
    font-size: 0.5em;
    color: #b0b0c8;
  }
---

<!-- _class: title -->

# Platform Engineering

## Séance d'ouverture · M2 Ops

<!--
Déjà court. Pas de retouche.
-->

---

## Le point de départ

- Vous allez construire un produit. Ses utilisateurs sont dans la salle d'à côté.
- Ne partez pas de l'organisation. Partez de ce qu'ils construisent.

---

## $ ~ whoami
### Luc Chmielowski

- Platform Engineer, actuellement @ Leetchi
- Mainteneur open-source @ CNCF
- Au delà de vous apprendre kubernetes, je serai celui qui vous demande **pourquoi**.

<br/>

> En tant que platform engineer je construis des plateformes infra pour des devs, ce cours vient donc de ce que j'ai appris à leurs dépens.

---

<!-- _class: section -->

<div class="section-num">01</div>

# Contexte

<p class="subtitle">Le projet, et pour qui vous le construisez</p>

---

<p class="eyebrow">Contexte</p>

## Vos clients, les développeurs

- Les équipes dev ne sont pas (seulement) vos camarades de promo, **ce sont vos utilisateurs**, 
- Un seul critère : est-ce que ça les fait avancer plus vite avec moins de charge cognitive ?
- Une plateforme classique a un droit de passage. Vous ne l'avez pas.

<!--
Elles ont des délais, elles doivent livrer. Une équipe plateforme construit quelque chose que personne n'est obligé d'utiliser. Utiliser un droit de passage revient à un échec de conception. Phrase centrale de la séance, tout le reste en découle.
-->

---

<!-- _class: section -->

<div class="section-num">02</div>

# Attentes

<p class="subtitle">Ce qu'on attend de vous, et comment c'est évalué</p>

---

<p class="eyebrow">Attentes</p>

## Conception complète, aucune techno imposée

- Vous choisissez, vous mettez en œuvre, vous défendez.

<!--
Une contrainte technique s'y ajoute, on y revient à la fin de cette section.
-->

---

<p class="eyebrow">Attentes</p>

## L'IA est autorisée, et évaluée

- Autorisée partout, sur tout.
- Toute production assistée doit être expliquée, testée, contestée, modifiée par son auteur, en direct, sans préparation.

<!--
La compétence mesurée est la supervision et la décision, pas la capacité à obtenir un artefact plausible.
-->

---

<p class="eyebrow">Attentes</p>

## Deux transferts, deux natures

| | Dev → Ops | Ops → Dev |
|---|---|---|
| Sujet | Architecture distribuée | Utiliser votre plateforme |
| Objectif | Comprendre | Autonomie |
| Vous n'avez pas à | Savoir l'implémenter | Leur apprendre à opérer un cluster |
| Preuve | Vous challengez avant que ça devienne votre incident | Un dev déploie et diagnostique sans vous |

<!--
Ils sont vos utilisateurs, pas vos successeurs.
-->

---

<p class="eyebrow">Attentes</p>

## Ce que vous transmettez

| Bloc | Le dev doit savoir |
|---|---|
| Runtime | Déployer, savoir si c'est parti, comprendre un pod qui ne démarre pas |
| Livraison | Commit → prod, promotion, retour arrière |
| Observabilité : usage | Logs, trace, réagir à une alerte |
| Observabilité : code | Contrat d'instrumentation |
| Frontières | Ce qu'il fait seul / ce qui passe par vous / sortie de secours |

<!--
Le périmètre de ce transfert = périmètre de votre chemin de déploiement. Hors périmètre : installation du cluster, topologie, réseau, stockage, tenancy, quotas.
-->

---

<p class="eyebrow">Attentes</p>

## Trois points de méthode sur les transferts

- 1. Transmettre n'est pas relayer
- 2. C'est un flux, pas une séance
- 3. Un transfert difficile à écrire signale un chemin trop complexe

<!--
1. Envoyer un lien vers le dépôt n'est pas un transfert, le matériel doit être le vôtre.
2. Ça grandit avec votre plateforme, vous ne transmettez pas ce que vous n'avez pas encore choisi.
3. Si le transfert est dur à écrire, votre chemin est trop complexe, c'est un signal de conception.
Les deux transferts ont une date, un format, un livrable, décidés entre vous et les équipes dev.
-->

---

<p class="eyebrow">Attentes</p>

## Les jalons, indicatifs

<div class="timeline">
  <div class="timeline-node">
    <div class="timeline-dot accent">S2</div>
    <div class="timeline-label">Premier déploiement</div>
    <div class="timeline-desc">En production</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot">S4</div>
    <div class="timeline-label">Chaîne de livraison</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot">S6</div>
    <div class="timeline-label">Exploitation</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot">S8</div>
    <div class="timeline-label">Validation finale</div>
  </div>
</div>

<!--
Répondent à une seule question : êtes-vous en retard ou non ? Rien ne démarre avant que le cluster existe : le socle est votre chemin critique. S2 n'est pas indicatif comme les autres : 22 développeurs attendent derrière. Indicatif ne veut pas dire sans conséquence.
-->

---

<p class="eyebrow">Attentes</p>

## Défendre, pas justifier

<div class="quad">
  <div class="quad-card">
    <h4>Direction</h4>
    <p>Tenir sous contradiction, ne pas juste prouver qu'on avait raison.</p>
  </div>
  <div class="quad-card">
    <h4>Moment</h4>
    <p>Au moment de la décision, pas après coup, en connaissant déjà le résultat.</p>
  </div>
  <div class="quad-card">
    <h4>Alternatives</h4>
    <p>Savoir pourquoi elles ne convenaient pas ICI, pas juste les mentionner.</p>
  </div>
  <div class="quad-card">
    <h4>Limites</h4>
    <p>Connaître la condition d'invalidité, pas les minimiser.</p>
  </div>
</div>

<!--
Une décision dont on ne peut pas énoncer les conditions d'invalidité n'a pas été prise. Elle a été subie.
-->

---

<p class="eyebrow">Attentes</p>

## Les ADR

- Au moment de la décision = défense / Après coup = justification.

<div class="quad">
  <div class="quad-card">
    <h4>Contexte</h4>
    <p>La situation qui force la décision, pourquoi maintenant, pourquoi ce choix devient nécessaire.</p>
  </div>
  <div class="quad-card">
    <h4>Décision</h4>
    <p>Ce qui est tranché, en une phrase claire.</p>
  </div>
  <div class="quad-card">
    <h4>Alternatives écartées</h4>
    <p>Et pourquoi elles ne convenaient pas ICI, dans votre contexte, pas dans l'absolu.</p>
  </div>
  <div class="quad-card">
    <h4>Signal de révision</h4>
    <p>Ce qui vous ferait changer d'avis, observable, pas une bonne intention.</p>
  </div>
</div>

<!--
Format complet dans EXIGENCES.md.
-->

---

<p class="eyebrow">Attentes</p>

## Exemple d'ADR

<div class="quad">
  <div class="quad-card">
    <h4>Contexte</h4>
    <p>Deux services demandent un accès direct à la même base pour éviter une duplication de données.</p>
  </div>
  <div class="quad-card">
    <h4>Décision</h4>
    <p>Chaque service garde sa propre base. La duplication contrôlée remplace l'accès direct.</p>
  </div>
  <div class="quad-card">
    <h4>Alternatives écartées</h4>
    <p>Base partagée : plus simple à court terme, mais interdit toute restauration ciblée. Rejetée pour ce système, pas dans l'absolu.</p>
  </div>
  <div class="quad-card">
    <h4>Signal de révision</h4>
    <p>Si la duplication cause une dérive de données que la réconciliation ne résout plus, la décision est rouverte.</p>
  </div>
</div>

<!--
Cet exemple reprend directement la contrainte « pas de base partagée entre services » et le concept de réconciliation du Pilier 1 : un ADR n'invente pas un nouveau vocabulaire, il applique les concepts déjà posés à une décision concrète.
-->

---

<p class="eyebrow">Attentes</p>

## La consultation : RFC et review d'ADR

- 1. Une question précise (pas « qu'en pensez-vous », « avons-nous raté un scénario d'échec »)
- 2. Une date de clôture
- 3. Un résumé des retours par l'auteur

<!--
Une RFC = décision non prise, soumise à feedback. Une review d'ADR = décision presque prise, soumise à vérification. Un retour ignoré sans explication dit « vos avis ne comptent pas ». Une RFC dont les retours ne sont jamais résumés est une boîte aux lettres.
-->

---

<p class="eyebrow">Attentes</p>

## Trois exemples de questions de défense

- 1. Quelle dimension d'isolation n'assurez-vous pas, quel scénario en profiterait ?
- 2. Est-ce que votre plateforme accélère ou impose ? Quelle preuve en avez vous ?
- 3. Dans quelles conditions cette décision devient-elle mauvaise ?

<!--
Aucune n'a de réponse générique, seulement si vous connaissez votre système.
-->

---

<p class="eyebrow">Attentes</p>

## Ce qui sera évalué

- 1. Test du chemin de déploiement, chronométré, sans aide
- 2. Incidents injectés, détection, qualification, décision, restauration, post-mortem
- 3. Interrogations individuelles, point nommé, contrainte qui change en direct

<!--
L'évaluation porte sur les décisions et leur défense, pas sur la présence d'une implémentation.
-->

---

<p class="eyebrow">Attentes</p>

## Communiquer techniquement

<div class="trio">
  <div class="quad-card">
    <h4>Partager</h4>
    <p><strong>Post-mortem, runbook.</strong> Après un apprentissage, ce que quelqu'un devra relire plus tard.</p>
  </div>
  <div class="quad-card">
    <h4>Consulter</h4>
    <p><strong>RFC, review d'ADR.</strong> Avant de décider, vérifier qu'on n'a rien raté.</p>
  </div>
  <div class="quad-card">
    <h4>Décider</h4>
    <p><strong>ADR.</strong> Après avoir tranché, trace de la décision.</p>
  </div>
</div>

<!--
La plupart des désaccords qui dégénèrent viennent d'une décision bien prise, mal communiquée. La review croisée : avant de figer un ADR, une personne extérieure pose une seule question : « quelle est la condition qui vous ferait changer d'avis ? » Pas pour bloquer, pour révéler ce qui n'a pas été pensé.
-->

---

<p class="eyebrow">Attentes</p>

## Quand écrire

<div class="decision">
  <div class="checklist">
    <div class="check-item"><span class="check-num">1</span>Décision difficile à annuler ?</div>
    <div class="check-item"><span class="check-num">2</span>Engage plusieurs équipes ?</div>
    <div class="check-item"><span class="check-num">3</span>Pertinente dans 6 semaines ?</div>
    <div class="check-item"><span class="check-num">4</span>Quelqu'un devra la comprendre sans vous ?</div>
  </div>
  <div class="verdicts">
    <div class="verdict low">
      <div class="verdict-label">0 à 1 oui</div>
      <div class="verdict-value">Discussion orale, décision notée dans le fil du canal</div>
    </div>
    <div class="verdict high">
      <div class="verdict-label">2 oui ou plus</div>
      <div class="verdict-value">ADR ou RFC</div>
    </div>
  </div>
</div>

<!--
Écrire trop tue la lecture. Si tout est important, rien ne l'est.
-->

---

<p class="eyebrow">Attentes</p>

## Kubernetes on-premise : la seule contrainte

- Élasticité illimitée → somme fixe
- Répartiteur / stockage / identité auto-fournis → à construire
- Deux équipes, même capacité demandée : qui décide, sur quel critère ?

<!--
Le on-prem n'est pas une punition : c'est la partie la plus proche du métier réel. En infra louée, « ça ne tient pas la charge » a une réponse paresseuse : payer. Ici cette réponse n'existe pas. Vous serez obligés d'arbitrer explicitement, par écrit. Cette contrainte cadre tout ce qui vient : chemin goudronné, charge finie, arbitrage. La partie théorie qui suit en découle directement.
-->

---

<p class="eyebrow">Attentes</p>

## Kubernetes : contrainte et outil

- La contrainte devient la méthode : c'est aussi comment vous ferez respecter les cinq piliers.

<div class="quad">
  <div class="quad-card">
    <h4>Réconciliation continue</h4>
    <p>Vous déclarez l'état voulu, Kubernetes le fait respecter en continu, pas seulement au moment du déploiement.</p>
  </div>
  <div class="quad-card">
    <h4>Runtime commun aux Dev et Ops</h4>
    <p>Pas une couche que vous cachez : les Dev déploient directement dessus, le vocabulaire (pod, service, namespace) est partagé.</p>
  </div>
</div>

<!--
La réconciliation continue est le mécanisme central : un contrôleur compare en boucle l'état réel à l'état déclaré et corrige les écarts. C'est ce qui vous permettra d'exprimer et de faire tenir les contraintes de chaque pilier sans intervention manuelle à chaque fois. Les Dev ne verront pas Kubernetes à travers une abstraction complète : c'est leur outil aussi, pas seulement le vôtre.
-->

---

<!-- _class: section -->

<div class="section-num">03</div>

# Platform Engineering

<p class="subtitle">D'où ça vient, pourquoi ça existe</p>

---

<p class="eyebrow">Platform Engineering</p>

## Trois âges

<div class="timeline">
  <div class="timeline-node">
    <div class="timeline-dot wide">Ops</div>
    <div class="timeline-label">Quelqu'un tient la prod</div>
    <div class="timeline-desc"><span class="ok">Résolu :</span> continuité de service<br><span class="bad">Créé :</span> mur build/run</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot wide">DevOps</div>
    <div class="timeline-label">Le mur tombe</div>
    <div class="timeline-desc"><span class="ok">Résolu :</span> propriété de la prod<br><span class="bad">Créé :</span> chaque équipe doit tout savoir</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot wide accent">Platform</div>
    <div class="timeline-label">Mutualiser sans reconstruire le mur</div>
    <div class="timeline-desc"><span class="ok">Résolu :</span> duplication de charge<br><span class="bad">Créé :</span> une plateforme que personne n'utilise</div>
  </div>
</div>

<!--
Pas un retour aux Ops. La différence tient en un mot : vous n'avez pas de droit de passage.
-->

---

<p class="eyebrow">Platform Engineering</p>

## Le changement de mindset : produit, pas service interne

- DevOps : chaque équipe possède son infra, « you build it, you run it ».
- Platform Engineering : une équipe construit un produit, les autres équipes sont ses clients.

<div class="quad">
  <div class="quad-card">
    <h4>Roadmap</h4>
    <p>Pilotée par le besoin des utilisateurs, pas une liste de tickets à traiter.</p>
  </div>
  <div class="quad-card">
    <h4>Utilisateurs, pas tickets</h4>
    <p>Vous parlez à vos consommateurs pour comprendre leur usage, pas seulement pour répondre à leurs demandes.</p>
  </div>
  <div class="quad-card">
    <h4>Itération sur feedback</h4>
    <p>Le produit évolue selon ce qui est réellement utilisé, pas selon ce qui semble complet.</p>
  </div>
  <div class="quad-card">
    <h4>Adoption, pas obligation</h4>
    <p>Un produit se mesure à son taux d'adoption volontaire, personne n'est forcé de l'utiliser.</p>
  </div>
</div>

<!--
Ce basculement vers l'état d'esprit produit est reconnu comme le principe central du platform engineering (Humanitec, CNCF Platforms White Paper) : traiter votre plateforme interne comme un produit, et les équipes de développement comme vos clients, pas comme des utilisateurs captifs d'un service imposé. Ça change ce que vous priorisez et comment vous mesurez le succès. Ça rejoint directement la slide « Vos clients, les développeurs » : une plateforme classique a un droit de passage, vous ne l'avez pas, parce que vous êtes un produit, pas une autorité.
-->

---

<p class="eyebrow">Platform Engineering</p>

## Pourquoi le DevOps casse à l'échelle

- Fonctionne à 8 équipes. Casse à 40.

<div class="trio">
  <div class="quad-card">
    <h4>Pipelines</h4>
    <p>7 manières différentes de déployer. Aucune mutualisation.</p>
  </div>
  <div class="quad-card">
    <h4>Observabilité</h4>
    <p>Chaque équipe reconstruit sa propre pile de logs, métriques, traces.</p>
  </div>
  <div class="quad-card">
    <h4>Secrets</h4>
    <p>Gestion et rotation réinventées équipe par équipe.</p>
  </div>
</div>

<!--
"You build it, you run it" : chaque équipe reconstruit son pipeline, sa pile d'observabilité, sa gestion de secrets. Des équipes produit qui passent la moitié de leur temps sur de l'infra. Le platform engineering répond à ce coût de duplication.
-->

---

<p class="eyebrow">Platform Engineering</p>

## Pourquoi une plateforme existe

- Charge finie. 7 responsabilités ≠ 7 domaines maîtrisés.

<div class="trio">
  <div class="quad-card">
    <h4>Domaine métier</h4>
    <p>Ce pour quoi l'équipe existe, la seule chose qu'elle devrait avoir à maîtriser.</p>
  </div>
  <div class="quad-card">
    <h4>Infrastructure</h4>
    <p>Base de données, pipeline de build, réseau : trois domaines techniques en plus.</p>
  </div>
  <div class="quad-card">
    <h4>Exploitation</h4>
    <p>Secrets, alerting : la production qu'il faut aussi tenir.</p>
  </div>
</div>

- Une plateforme retire de la charge, ne la déplace pas, ne l'ajoute pas.

<!--
Pourquoi une organisation paie des gens à ne pas livrer de fonctionnalité client ? Une équipe produit a une capacité de raisonnement finie : domaine métier, base, pipeline, réseau, secrets, build, alerting. Tenir les sept, c'est n'en tenir aucun bien.
-->

---

<p class="eyebrow">Platform Engineering</p>

## « Avec l'IA, chacun code ce dont il a besoin »

- Générer un pipeline sur mesure prend une heure. Le faire tourner trois ans, non.

<div class="trio">
  <div class="quad-card">
    <h4>Ce que l'IA accélère</h4>
    <p>Écrire : pipeline, dashboard, scaffolding d'API. Le temps de construction s'effondre.</p>
  </div>
  <div class="quad-card">
    <h4>Ce qu'elle ne retire pas</h4>
    <p>Tenir en prod : patch de sécurité, dérive de configuration, l'incident à 3h sur un outil que personne d'autre ne comprend.</p>
  </div>
  <div class="quad-card">
    <h4>Ce qu'elle aggrave</h4>
    <p>Chaque équipe génère sa propre variante. La duplication du slide précédent, produite plus vite, par des équipes qui ne se parlent pas plus qu'avant.</p>
  </div>
</div>

- La plateforme n'est plus en concurrence avec « je le code moi-même ». Elle décide quelle part de ce que l'IA génère devient un chemin partagé, plutôt qu'un artefact que son auteur est seul à savoir faire tourner.

<!--
L'objection mérite d'être prise au sérieux, pas balayée. Elle a raison sur un point : le coût de construction s'effondre. Elle a tort de s'arrêter là. La loi de Conway (slide « La loi de Conway ») ne se négocie pas avec un modèle de langage : des équipes qui ne se parlent pas produisent N variantes du même pipeline, pas une intégration. Et la charge cognitive qui suit ne disparaît pas parce que le code a été généré au lieu d'être tapé à la main — elle se déplace vers celui qui doit comprendre, trois ans plus tard, ce qu'un modèle a produit sans jamais expliciter pourquoi.
-->

---

<p class="eyebrow">Platform Engineering</p>

## Charge cognitive et Thinnest Viable Platform

- Le vocabulaire du platform engineering vient d'un seul livre : Team Topologies (Skelton &amp; Pais, 2019).

<div class="quad">
  <div class="quad-card">
    <h4>Charge cognitive</h4>
    <p>La charge mentale qu'un dev doit porter pour faire son travail. Domaine métier, mais aussi tout ce que personne d'autre ne prend en charge.</p>
  </div>
  <div class="quad-card">
    <h4>Thinnest Viable Platform</h4>
    <p>Pas la plateforme la plus complète possible. La plus fine qui réduit vraiment la charge, rien de plus.</p>
  </div>
  <div class="quad-card">
    <h4>Le risque inverse</h4>
    <p>Une plateforme trop épaisse devient elle-même une charge cognitive supplémentaire, voir le test hebdomadaire qui suit.</p>
  </div>
  <div class="quad-card">
    <h4>Où ça s'applique</h4>
    <p>Le chemin goudronné, plus loin dans cette séance, est une application directe du TVP.</p>
  </div>
</div>

<!--
Cognitive load et Thinnest Viable Platform sont les deux termes centraux de Team Topologies (Skelton & Pais) pour décrire ce que le platform engineering essaie de faire. Vous les recroiserez partout dans la vraie littérature du domaine : PlatformCon, CNCF Platforms White Paper. Autant les avoir maintenant plutôt que de redécouvrir le vocabulaire plus tard pour un concept déjà connu.
-->

---

<p class="eyebrow">Platform Engineering</p>

## Team Topologies

<div class="quad">
  <div class="quad-card">
    <h4>Stream-aligned</h4>
    <p>Responsable d'un produit ou d'un service, de bout en bout.</p>
  </div>
  <div class="quad-card">
    <h4>Platform</h4>
    <p>Réduit la charge cognitive des autres équipes en leur fournissant du self-service.</p>
  </div>
  <div class="quad-card">
    <h4>Enabling</h4>
    <p>Une équipe temporaire d'experts qui monte les autres en compétence, puis se retire.</p>
  </div>
  <div class="quad-card">
    <h4>Complicated-subsystem</h4>
    <p>Possède une brique trop complexe ou trop spécialisée pour être partagée.</p>
  </div>
</div>

<!--
Quatre types d'équipe qui couvrent la quasi-totalité des organisations tech réelles. Une équipe sécurité ou data qui vient former les autres puis repart : enabling. Une équipe qui possède un moteur de pricing ou un système de paiement trop complexe pour être partagé : complicated-subsystem. Les connaître maintenant évite de redécouvrir le vocabulaire au premier jour d'un vrai poste.
-->

---

<p class="eyebrow">Platform Engineering</p>

## Le test hebdomadaire

- Chaque semaine, une question : ce que vous avez livré a-t-il vraiment retiré de la charge, ou juste changé de forme ?

<div class="quad">
  <div class="quad-card">
    <h4>Un gabarit copié sans vous</h4>
    <p>L'équipe l'adapte seule, sans repasser par vous.</p>
    <span class="badge good">Charge retirée</span>
  </div>
  <div class="quad-card">
    <h4>Une abstraction à comprendre en plus</h4>
    <p>Elle s'ajoute à ce qu'elle était censée cacher.</p>
    <span class="badge bad">Charge ajoutée</span>
  </div>
  <div class="quad-card">
    <h4>Un formulaire qui déclenche une action manuelle</h4>
    <p>Quelqu'un doit encore traiter la demande.</p>
    <span class="badge moved">Charge déplacée, délai ajouté</span>
  </div>
  <div class="quad-card">
    <h4>Une doc de 40 pages sur votre outil maison</h4>
    <p>Présentée comme un service, elle en est un de plus à maintenir.</p>
    <span class="badge bad">Charge ajoutée, déguisée</span>
  </div>
</div>

<!--
La troisième ligne est la plus fréquente et la plus difficile à voir de l'intérieur : ça ressemble à du service, tout le monde est poli, et pourtant chaque déploiement attend quelqu'un.
-->

---

<!-- _class: section -->

<div class="section-num">04</div>

# Concevoir

<p class="subtitle">Comment construire un chemin qu'on choisit d'emprunter</p>

---

<p class="eyebrow">Concevoir</p>

## Le chemin goudronné

- Le trajet le plus facile pour faire ce que 80 % des équipes font 80 % du temps.

<div class="trio">
  <div class="quad-card">
    <h4>Optionnel</h4>
    <p>Sinon, c'est un mur.</p>
  </div>
  <div class="quad-card">
    <h4>Plus rapide que l'alternative</h4>
    <p>Sinon, personne ne le prend.</p>
  </div>
  <div class="quad-card">
    <h4>Sortie documentée</h4>
    <p>Sinon, les sorties se font en douce.</p>
  </div>
</div>

- Couvre le cas majoritaire, pas tous les cas.

<!--
Les trois propriétés sont nécessaires ensemble : retirer une seule suffit à tout casser.
-->

---

<p class="eyebrow">Concevoir</p>

## Trois modes d'interaction

<div class="trio">
  <div class="quad-card">
    <h4>Self-service</h4>
    <p>L'équipe consomme sans vous parler. État cible : l'interaction minimale n'est pas un manque de service, c'est le signe que ça marche.</p>
  </div>
  <div class="quad-card">
    <h4>Collaboration</h4>
    <p>Vous résolvez ensemble un problème encore mal défini. Doit avoir une date de fin, sinon elle devient confortable et remplace l'abstraction qu'elle devrait produire.</p>
  </div>
  <div class="quad-card">
    <h4>Accompagnement</h4>
    <p>Vous rendez l'équipe autonome sans prendre le sujet à votre charge. C'est le mode du transfert Kubernetes vers les Dev.</p>
  </div>
</div>

<!--
Erreur classique : rester en collaboration permanente parce que c'est gratifiant, et ne jamais produire l'abstraction qui la rendrait inutile.
-->

---

<p class="eyebrow">Concevoir</p>

## Le contournement est votre meilleur indicateur

- Un contournement signale un chemin officiel trop lent.
- Pas du platform engineering : outils sans plateforme, guichet de tickets, décider seuls, plateforme parfaite sur produit cassé.

<!--
Un contournement reproché ne sera plus signalé : vous perdez votre meilleur capteur.
-->

---

<!-- _class: section -->

<div class="section-num">05</div>

# Votre organisation

<p class="subtitle">Comment vous êtes structurés</p>

---

<p class="eyebrow">Votre organisation</p>

## La loi de Conway

- Une architecture copie sa structure de communication.

<div class="diagram">
<img src="images/conway.png" alt="La loi de Conway : équipes qui communiquent produisent un système intégré, équipes qui s'ignorent produisent des composants qui ne s'intègrent pas" style="width:100%;max-width:680px;" />
</div>

<!--
Deux sous-groupes qui ne se parlent pas produisent deux composants qui ne s'intègrent pas. C'est le principe qui a guidé la structure ci-dessous.
-->

---

<p class="eyebrow">Votre organisation</p>

## La structure possible

<div class="diagram">
<img src="images/team-topologies.png" alt="5 squads mixtes en intégration quotidienne, 3 équipes transverses en rotation hebdomadaire" style="width:100%;max-width:740px;" />
</div>

<!--
Ce n'est pas un choix laissé à cette promotion : la structure a été validée avec les équipes de développement. C'est le modèle « noyau + embarqués » : les Ops embarqués assurent la proximité du besoin, les équipes transverses assurent la boucle de retour structurelle. Un modèle purement centralisé produit une file de tickets ; un modèle purement embarqué perd toute mutualisation. C'est pourquoi les deux dispositifs coexistent.
-->

---

<p class="eyebrow">Votre organisation</p>

## Le rôle du roulement transverse

- Chaque semaine, chaque équipe transverse change de sujet.
- 1. Moins d'interruptions dans les squads
- 2. Chacun voit la friction réelle
- 3. Passation obligatoire : continuité et montée en compétence

<!--
Le roulement transverse est le canal structurel de remontée de friction. S'il cesse de tourner, ou si la passation devient superficielle, l'organisation perd sa boucle de retour. Publiez ce que chaque équipe possède, ne possède pas, et comment la joindre.
-->

---

<!-- _class: section -->

<div class="section-num">06</div>

# Les piliers

<p class="subtitle">Cinq piliers, cinq conséquences opérationnelles</p>

---

<p class="eyebrow">Les piliers</p>

## Une table commune dev / ops

<div class="chip-row">
  <span class="chip">Architecture distribuée</span>
  <span class="chip">Delivery</span>
  <span class="chip">Platform Engineering</span>
  <span class="chip">Fiabilité</span>
  <span class="chip">Sécurité</span>
</div>

<!--
Vous l'avez déjà vue côté Dev. On ne réexplique pas chaque question. La suite en donne un exemple concret par pilier, côté Ops.
-->

---

<p class="eyebrow">Architecture distribuée</p>

## Vous n'écrirez pas leur architecture

- Vous ne décidez pas leur découpage métier. Vous décidez et imposez les contraintes de plateforme qui l'encadrent.

<div class="trio">
  <div class="quad-card">
    <h4>Ils décident</h4>
    <p>Flux asynchrone → vous concevez un courtier exploitable : rétention, rejeu, supervision.</p>
  </div>
  <div class="quad-card">
    <h4>Ils décident</h4>
    <p>Traitement non idempotent → vous concevez la déduplication, jamais d'auto-scaling des consommateurs sans elle.</p>
  </div>
  <div class="quad-card">
    <h4>Vous imposez</h4>
    <p>Pas de base partagée entre services, contrainte de plateforme, pas une négociation.</p>
  </div>
</div>

<div class="quad">
  <div class="quad-card">
    <h4>Cohérence distribuée</h4>
    <p>Ils choisissent la cohérence éventuelle plutôt que forte : vous absorbez le risque de lecture obsolète, pas eux.</p>
  </div>
  <div class="quad-card">
    <h4>Réconciliation</h4>
    <p>Un mécanisme qui détecte et corrige les divergences entre services, sans lui la cohérence éventuelle ne redevient jamais cohérente.</p>
  </div>
</div>

<!--
Pilier 2, Delivery : on construit une fois, on promeut le même artefact. Reconstruire à chaque environnement, c'est recompiler à un instant différent : ce qui est testé n'est pas ce qui part en production.
-->

---

<p class="eyebrow">Architecture distribuée</p>

## Les data-scientists ont fait tomber la prod

<span class="example-tag">Exemple vécu</span>

<div class="timeline">
  <div class="timeline-node">
    <div class="timeline-dot">1</div>
    <div class="timeline-label">Pas de mécanisme dédié</div>
    <div class="timeline-desc">Aucun accès aux données prévu pour les data-scientists</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot">2</div>
    <div class="timeline-label">Ils appellent la prod directement</div>
    <div class="timeline-desc">Requêtes analytiques lourdes sur la base transactionnelle</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot accent">3</div>
    <div class="timeline-label">La base tombe</div>
    <div class="timeline-desc">Le service qui dépend de cette même base tombe avec elle</div>
  </div>
</div>

<!--
Pas un manque de discipline des data-scientists : un besoin réel (accéder aux données) sans chemin officiel pour le satisfaire. Ça rejoint directement la contrainte « pas de base partagée entre services » de la slide précédente : sans mécanisme dédié, le contournement le plus simple est d'appeler la prod directement.
-->

---

<p class="eyebrow">Delivery</p>

## Delivery : les concepts clés

<div class="trio">
  <div class="quad-card">
    <h4>Build once, promote everywhere</h4>
    <p>L'artefact testé est l'artefact déployé, pas de reconstruction entre environnements.</p>
  </div>
  <div class="quad-card">
    <h4>Promotion entre environnements</h4>
    <p>Recompiler à chaque étape, c'est tester autre chose que ce qui part en production.</p>
  </div>
  <div class="quad-card">
    <h4>Retour arrière</h4>
    <p>Un mécanisme aussi rapide que le déploiement lui-même, pas un espoir.</p>
  </div>
</div>

<div class="quad">
  <div class="quad-card">
    <h4>Feature flags</h4>
    <p>Découpler déploiement (le code arrive) et release (l'utilisateur le voit). Le retour arrière le plus rapide n'est parfois pas un redéploiement.</p>
  </div>
  <div class="quad-card">
    <h4>Migration de données</h4>
    <p>Évolution du schéma synchronisée avec le code, jamais l'inverse. Une migration non réversible transforme un retour arrière logiciel en incident de données.</p>
  </div>
</div>

<!--
Reconstruire à chaque environnement revient à recompiler à un instant différent : ce qui a été testé n'est plus ce qui part en production. Le retour arrière doit être aussi rapide et aussi peu risqué que le déploiement lui-même, sinon il ne sera jamais utilisé en situation réelle.
-->

---

<p class="eyebrow">Delivery</p>

## Rollback sur latest, mauvaise version, mauvais schéma

<span class="example-tag">Exemple vécu</span>

<div class="timeline">
  <div class="timeline-node">
    <div class="timeline-dot">1</div>
    <div class="timeline-label">Rollback lancé</div>
    <div class="timeline-desc">Sur le tag Docker latest, pas une version épinglée</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot">2</div>
    <div class="timeline-label">Mauvaise version déployée</div>
    <div class="timeline-desc">Latest avait bougé depuis, ce n'est plus l'image d'avant</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot accent">3</div>
    <div class="timeline-label">Le service crash</div>
    <div class="timeline-desc">Le schéma de la base ne correspond plus à ce que ce code attend</div>
  </div>
</div>

<!--
Deux violations du même principe à la fois : build once promote everywhere suppose un artefact identifié de manière unique, latest n'en est pas un, il bouge. Et la migration de données doit être synchronisée avec le code, pas l'inverse : le schéma avait avancé, le code rollbacké attendait l'ancien. Le retour arrière n'était pas un mécanisme, c'était un pari.
-->

---

<p class="eyebrow">Platform Engineering</p>

## Platform Engineering : les concepts clés

<div class="quad">
  <div class="quad-card">
    <h4>Golden path</h4>
    <p>Mesuré, pas déclaré.</p>
  </div>
  <div class="quad-card">
    <h4>DORA &amp; SPACE</h4>
    <p>Fréquence de déploiement, lead time, taux d'échec, temps de restauration, plus la satisfaction et l'activité des équipes : ce qui prouve que la plateforme accélère, pas juste ce qu'elle prétend faire.</p>
  </div>
  <div class="quad-card">
    <h4>Developer Portal</h4>
    <p>Un catalogue self-service des services, templates et golden paths : l'interface, pas juste le contenu.</p>
  </div>
  <div class="quad-card">
    <h4>Developer Experience</h4>
    <p>Ce que ça coûte, en friction et en temps, pour qu'un dev fasse son travail : la métrique qui justifie toutes les autres.</p>
  </div>
</div>

<!--
La section théorique a couvert le pourquoi (chemin goudronné, modes d'interaction). Health checks, readiness et l'observabilité relèvent de la fiabilité, pas d'ici. Ici, le concret de la plateforme comme produit : un chemin mesuré (pas déclaré), des preuves chiffrées que ça marche (DORA), une interface pour le consommer (portal), et la question qui les relie toutes : est-ce que ça réduit vraiment la friction du développeur ?
-->

---

<p class="eyebrow">Platform Engineering</p>

## Le bus de données de toute l'entreprise, construit en douce

<span class="example-tag">Exemple vécu</span>

<div class="timeline">
  <div class="timeline-node">
    <div class="timeline-dot">1</div>
    <div class="timeline-label">Le contournement</div>
    <div class="timeline-desc">Terraform était officiel, l'équipe la plus exigeante bascule sur CloudFormation</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot">2</div>
    <div class="timeline-label">Ça devient critique</div>
    <div class="timeline-desc">Ce qu'ils construisent devient le bus de données de toute l'entreprise</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot">3</div>
    <div class="timeline-label">La découverte</div>
    <div class="timeline-desc">Quelques semaines après</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot accent">4</div>
    <div class="timeline-label">Le nettoyage</div>
    <div class="timeline-desc">Deux ans pour s'en débarrasser</div>
  </div>
</div>
<br /><br />

_Avec les coding-agents, ce genre de contournement se fait encore plus vite, et donc encore plus facilement sans que vous ne le voyiez._

<!--
Le diagnostic n'est pas « ils ont triché ». Le chemin officiel était plus lent que le besoin. La découverte n'a pas traîné, quelques semaines suffisent pour qu'un contournement remonte. Le vrai coût est venu après : désinstaller quelque chose qui était déjà la colonne vertébrale du système a pris deux ans.
-->

---

<p class="eyebrow">Fiabilité</p>

## Fiabilité : les concepts clés

<div class="quad">
  <div class="quad-card">
    <h4>Health checks &amp; readiness</h4>
    <p>La plateforme sait si le service peut réellement servir, pas juste s'il tourne.</p>
  </div>
  <div class="quad-card">
    <h4>Métriques, traces, logs</h4>
    <p>Le socle d'observabilité fourni par défaut, pas réinventé par chaque service.</p>
  </div>
  <div class="quad-card">
    <h4>Retry &amp; timeout</h4>
    <p>Réessayer sans borne transforme une lenteur en panne. Chaque appel a besoin d'un délai maximum et d'un nombre de tentatives limité.</p>
  </div>
  <div class="quad-card">
    <h4>Circuit breaker</h4>
    <p>Arrêter d'appeler un service défaillant plutôt que d'empiler les tentatives, ça protège l'appelant et laisse le temps au service de récupérer.</p>
  </div>
</div>

<div class="trio">
  <div class="quad-card">
    <h4>Rayon d'impact</h4>
    <p>Jusqu'où une panne se propage.</p>
  </div>
  <div class="quad-card">
    <h4>SLO, SLI, error budget</h4>
    <p>Pas disponibilité binaire, un budget d'indisponibilité mesuré sur une période.</p>
  </div>
  <div class="quad-card">
    <h4>Dégradation</h4>
    <p>Progressive vs propagation en cascade.</p>
  </div>
</div>

<!--
La fiabilité ne se résume pas à "up ou down". Un service qui répond en 6 secondes au lieu de 40ms n'est pas tombé, il dégrade. Le seuil auquel une dégradation devient une panne pour les appelants est une décision de conception, pas un fait donné par le système. Health checks, readiness et l'observabilité (métriques, traces, logs) sont les capteurs qui permettent de détecter la dégradation avant qu'elle devienne panne.
-->

---

<p class="eyebrow">Fiabilité</p>

## La contre-mesure a créé la panne

<span class="example-tag">Exemple vécu</span>

<div class="timeline">
  <div class="timeline-node">
    <div class="timeline-dot">1</div>
    <div class="timeline-label">Bug de perf corrigé</div>
    <div class="timeline-desc">Une requête base de données optimisée sur un service</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot">2</div>
    <div class="timeline-label">Le service absorbe x10</div>
    <div class="timeline-desc">60 → ~600 req/s : la lenteur qui limitait le trafic a disparu</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot accent">3</div>
    <div class="timeline-label">La base tombe</div>
    <div class="timeline-desc">Jamais dimensionnée pour ce volume, elle était protégée par la lenteur du service</div>
  </div>
</div>

<!--
Un correctif de performance bien intentionné a supprimé le goulot d'étranglement qui protégeait involontairement la base de données. Personne n'avait conçu cette protection : elle existait par accident, dans la lenteur du service. La corriger a révélé que la base n'avait jamais été dimensionnée pour le trafic réel que le service pouvait générer une fois performant.
-->

---

<p class="eyebrow">Sécurité</p>

## Sécurité : les concepts clés

<div class="trio">
  <div class="quad-card">
    <h4>Ce que peut faire, par défaut</h4>
    <p>Un compte, une chaîne de livraison, un agent.</p>
  </div>
  <div class="quad-card">
    <h4>Contrôle</h4>
    <p>Bloquant vs constaté.</p>
  </div>
  <div class="quad-card">
    <h4>Chaîne d'approvisionnement</h4>
    <p>Ce que vous n'avez pas écrit vous-même.</p>
  </div>
</div>

<div class="quad">
  <div class="quad-card">
    <h4>Trust boundaries</h4>
    <p>Chaque frontière de confiance mérite sa propre vérification, un service interne compromis n'hérite pas automatiquement des droits du système.</p>
  </div>
  <div class="quad-card">
    <h4>Propagation de l'identité</h4>
    <p>Qui a fait la demande à l'origine reste traçable de bout en bout, pas « le service A a appelé » mais « l'utilisateur X, via le service A ».</p>
  </div>
</div>

<!--
La question n'est pas « avez-vous un contrôle » mais « que peut faire quelque chose de compromis, et qui le bloque, à quel moment ». Un contrôle non-bloquant est une checklist, pas une garde-fou.
-->

---

<p class="eyebrow">Sécurité</p>

## Des PRs pour s'ajouter des droits

<span class="example-tag">Exemple vécu</span>

<div class="timeline">
  <div class="timeline-node">
    <div class="timeline-dot">1</div>
    <div class="timeline-label">Plateforme self-service pour AWS</div>
    <div class="timeline-desc">Une nouvelle plateforme centralise la gestion des comptes AWS</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot">2</div>
    <div class="timeline-label">Les devs s'ajoutent des droits par PR</div>
    <div class="timeline-desc">Une simple pull request suffit pour obtenir un accès</div>
  </div>
  <div class="timeline-node">
    <div class="timeline-dot accent">3</div>
    <div class="timeline-label">Les demandes explosent, sans justification</div>
    <div class="timeline-desc">Le volume grimpe, plus personne ne vérifie pourquoi le besoin existe</div>
  </div>
</div>

<!--
Le self-service a fait exactement ce qu'on lui demandait : retirer la friction. Le problème est que la friction retirée était aussi le seul moment où quelqu'un se demandait « pourquoi ce besoin ? ». Ça rejoint directement « Contrôle bloquant vs constaté » de la slide précédente : rendre une demande facile sans garder un contrôle dessus ne sécurise rien, ça déplace juste le problème après coup.
-->

---

<!-- _class: closing -->

## Pour finir

- 1. Votre livrable n'est pas un cluster : un produit dont les utilisateurs sont dans la salle d'à côté.
- 2. On vous évaluera sur ce que vous avez décidé et défendu.
- 3. Le meilleur indicateur : le moment où on cesse d'avoir besoin de vous parler, pas l'absence d'initiative, l'absence de friction.
- 4. Ces exemples sont tous des échecs. Délibéré.
