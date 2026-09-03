# Platform Engineering — DIIAGE

Support de cours sur le platform engineering, pour le projet fil rouge Dev/Ops de la DIIAGE : plateforme Kubernetes on-premise, produit destiné aux équipes de développement.

**Slides : https://lucchmielowski.github.io/platform-eng-diiage/**

## Contenu du repo

| Fichier / dossier | Contenu |
|---|---|
| [`slides.md`](./slides.md) | Le support de cours, au format [Marp](https://marp.app/) |
| [`MANIFESTO.md`](./MANIFESTO.md) | Les dix principes qui cadrent les décisions du cours — les ADR se jugent par rapport à ce cadre, pas l'inverse |
| [`examples/adr.md`](./examples/adr.md) | Exemple complet d'ADR (Architecture Decision Record) |
| [`examples/rfc.md`](./examples/rfc.md) | Exemple complet de RFC, y compris une esquisse technique soumise à relecture, qui débouche sur l'ADR ci-dessus |
| [`images/`](./images) | Diagrammes utilisés dans les slides |

## Build local

Les slides sont écrites en Markdown (Marp) et compilées en HTML via [`@marp-team/marp-cli`](https://github.com/marp-team/marp-cli).

```bash
npx @marp-team/marp-cli@4 slides.md --html -o dist/index.html
cp -r images dist/images
```

Ou en mode présentation, avec rechargement à chaud :

```bash
npx @marp-team/marp-cli@4 -s slides.md
```

## Déploiement

Le déploiement est automatisé par [`.github/workflows/deploy-slides.yml`](./.github/workflows/deploy-slides.yml) : chaque push sur `main` touchant `slides.md` ou `images/` reconstruit les slides et les publie sur GitHub Pages. Les pull requests déclenchent uniquement le build, pour valider qu'il ne casse pas avant merge.
