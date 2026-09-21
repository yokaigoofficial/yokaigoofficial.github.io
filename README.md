# Le site public — `yokaigoofficial.github.io`

Ce dossier est le site tel qu'il se dépose sur GitHub Pages : **tout son contenu va à la racine du
dépôt `yokaigoofficial/yokaigoofficial.github.io`**, fichiers cachés compris.

| Fichier | Rôle |
|---|---|
| `index.html` | La page d'accueil : l'application, les créatures, les données, le contact |
| `404.html` | La page qu'affiche GitHub Pages pour une adresse inexistante |
| `confidentialite.html`, `cgu.html` | Les documents légaux, **copiés depuis `docs/legal/`** |
| `style.css` | La seule feuille de style, partagée par l'accueil et la page 404 |
| `fonts/` | Les polices, servies d'ici |
| `assets/` | Les images : icône, mascotte, dessins du menu, neuf créatures, deux héros |
| `.nojekyll` | Dit à GitHub Pages de servir les fichiers tels quels, sans les passer par Jekyll |

## Déposer

Copier l'ensemble du dossier à la racine du dépôt du site, puis pousser. GitHub Pages publie en
une minute environ. Les adresses obtenues sont celles que les documents et l'application citent :

- `https://yokaigoofficial.github.io/confidentialite.html`
- `https://yokaigoofficial.github.io/cgu.html`

## Tenir à jour

**Les documents légaux ne se modifient pas ici.** Leur source est `docs/legal/*.md` ; après
`python tools/build_legal.py`, recopier `docs/legal/confidentialite.html` et `docs/legal/cgu.html`
dans ce dossier, puis redéposer.

**Les boutiques.** Les deux pastilles « Bientôt disponible » de l'accueil sont des `<span
class="store">` ; le jour de la mise en ligne, en faire des `<a class="store" href="…">` vers la
fiche de chaque boutique, et remplacer « Bientôt disponible » par « Télécharger ».

**Les chiffres de l'accueil** — 165 mondes, 619 créatures, 2 634 mots, 20 examens blancs — sont
ceux du pack de contenu au 21 septembre 2026. Ils se relisent dans `assets/content/content.sqlite`
(tables `world`, `monster`, `word`, `jlpt_paper`) à chaque changement de contenu.

## Ce que le site ne charge pas

Aucune police, aucun script, aucune image ne vient d'un serveur tiers. La politique de
confidentialité ne nomme que GitHub comme destinataire des visites, et une police chargée depuis
Google enverrait l'adresse de chaque visiteur ailleurs. Les polices sont celles de l'application,
sous licence SIL Open Font License 1.1 : Fredoka et Zen Maru Gothic réduites aux signes qu'elle
affiche, et un extrait de Noto Sans JP limité aux signes japonais de la page. Les textes des
licences sont dans `assets/fonts/OFL-*.txt` du projet.

## D'où viennent les images

- `assets/karakasa.webp` — `branding/karakasa.png`, le dessin de l'icône ;
- `assets/icone.png`, `assets/favicon.png` — l'icône Android, fond transparent ;
- `assets/menu/*.webp` — les dessins du menu (`branding/menu/`) et trois icônes du Drive du
  studio (écoute, omamori, JLPT) ;
- `assets/yokai/*.webp` — neuf créatures, copiées telles que l'application les embarque ;
- `assets/femme_japon.webp`, `assets/homme_japon.webp` — les deux héros, tenue japonaise.
