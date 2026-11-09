# Xilab.tech, site d'essai

Version d'essai du nouveau site Xilab.tech, construite avec Hugo 0.157 (extended).
Elle n'est pas indexée par les moteurs de recherche (`noindex` et `robots.txt`), et ne touche pas au site en ligne (dépôt `xilab-site`).

## Voir le site en local

```bash
hugo server
```

puis ouvrir l'adresse affichée.

## Où modifier quoi

| Contenu | Fichier |
|---|---|
| Briques de la chaîne (accueil) | `data/chaine.json` |
| Promesses éditeur / R&D | `data/promesses.json` |
| Base de cas | `data/cas.json` (+ libellés des filtres dans `data/etiquettes.json`) |
| Ressources R&D | `data/ressources.json` |
| Cas tests VoxFEM | `data/validation.json` (export de la campagne de non-régression) |
| Textes des pages | `layouts/partials/views/*.html` |
| Titres et descriptions des pages | `content/*.md` |
| Styles | `static/css/site.css` |
| Interactions | `static/js/site.js` |
| Vidéos, PDF, images | `static/media`, `static/docs`, `static/img` |

## Publication

Chaque push sur `main` déclenche `.github/workflows/hugo.yml`, qui construit le site et le publie sur GitHub Pages.
Dans les réglages du dépôt : *Settings → Pages → Source : GitHub Actions*.

Pour la mise en production, passer `essai = false` dans `hugo.toml` (retire le `noindex`).
