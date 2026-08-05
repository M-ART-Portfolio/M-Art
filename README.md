# M·Art — Portfolio artistique

Un regard personnel sur l'art qui marque. Œuvres et expositions choisies, présentées comme au musée : le mur, le cartel, mon regard, l'histoire — et mes photos de visite.

**Site en ligne :** https://m-art-portfolio.github.io/M-Art/

---

## Ajouter des photos (le plus simple)

Le site affiche lui-même les emplacements vides avec **le nom exact du fichier attendu** (ex. `taylor-3.jpg`). Il suffit d'uploader une photo portant ce nom à la racine du dépôt (`Add file → Upload files`) : elle apparaît toute seule, l'emplacement "à ajouter" disparaît.

Images attendues aujourd'hui :

| Page | Image principale | Galerie (onglet « En images ») |
|---|---|---|
| Collection Philippe Jabre | `jabre.jpg` | `jabre-1.jpg` → `jabre-6.jpg` |
| Henry Taylor | `taylor.jpg` | `taylor-1.jpg` → `taylor-6.jpg` |
| O'Keeffe & Moore | `okeeffe-moore.jpg` | `okm-1.jpg` → `okm-6.jpg` |
| La Dame en blanc | `lady.png` (déjà là) | `dame-1.jpg` → `dame-6.jpg` |

Conseil : `.jpg` de moins de 500 Ko (compresser sur [squoosh.app](https://squoosh.app) si besoin). Pas besoin de remplir les 6 cases — celles qui restent vides s'affichent élégamment.

## Modifier les textes

Chaque page est **autonome** : les textes français sont directement dans la page, et les deux langues (FR/EN) sont dans le bloc `I18N` en bas du fichier, clé par clé (`regard.p1`, `histoire.p2`, `hl1.t`…). Modifier une page ne peut rien casser ailleurs.

## Ajouter une nouvelle entrée

1. Dupliquer la page existante la plus proche (ex. `taylor.html`), la renommer (ex. `vague.html`).
2. Dans la nouvelle page : remplacer les textes FR dans le corps **et** les clés FR/EN du bloc `I18N` ; changer le nom d'image principale et le préfixe des 6 photos de galerie ; ajuster les liens « Entrée précédente / suivante » (ici et sur la page voisine).
3. Dans `index.html` : copier une carte de la grille, changer le lien, le numéro, le titre, l'artiste, les détails (et les clés `c5.*` dans le bloc `I18N` si le texte diffère en anglais).

## Structure du site

| Fichier | Rôle |
|---|---|
| `index.html` | Accueil : héro, citation, grille de la collection |
| `jabre.html`, `taylor.html`, `okeeffe-moore.html`, `dame-en-blanc.html` | Une page complète par entrée : mur de musée + cartel, 3 onglets (Mon regard / Histoire & contexte / En images), temps forts, navigation |
| `presentation.html` | Page À propos |
| `style.css` | Tout le design |

Chaque page embarque son propre JavaScript et son propre dictionnaire FR/EN : **aucune dépendance entre fichiers**, donc pas de panne en cascade.

## Fonctionnalités

- Bilingue FR / EN (choix mémorisé d'une page à l'autre)
- Emplacements photos automatiques : tant que l'image n'existe pas, la case indique le fichier à uploader
- Lightbox plein écran sur l'image principale et toutes les photos de galerie
- Responsive, animations douces, `prefers-reduced-motion` respecté
