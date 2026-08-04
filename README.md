# M·Art — Portfolio artistique

Un regard personnel sur l'art qui marque. Des œuvres choisies, présentées comme au musée : l'image, son cartel, mon regard et son histoire.

**Site en ligne :** https://flambardgautier-wq.github.io/M-Art/

---

## Ajouter une œuvre (3 étapes, ~5 minutes)

Tout le contenu vit dans **un seul fichier : `oeuvres.js`**. Pas besoin de toucher au HTML ni au CSS.

1. **Ajouter l'image** dans le dépôt (`Add file → Upload files`). Exemple : `vague.jpg`.
   Idéalement en `.jpg`, moins de 500 Ko (compresser sur [squoosh.app](https://squoosh.app) si besoin).

2. **Ouvrir `oeuvres.js`**, copier le bloc `MODÈLE` (tout en bas du fichier, dans les commentaires), le coller **après la dernière œuvre** de la liste `OEUVRES`, et le remplir : titre, artiste, année, technique, lieu, puis les paragraphes *Mon regard* et *Histoire & contexte*, en français et en anglais.
   ⚠️ Ne pas oublier la **virgule** entre deux œuvres.

3. **Commit.** C'est tout : la grille d'accueil et la page de l'œuvre se génèrent automatiquement.

---

## Structure du site

| Fichier | Rôle |
|---|---|
| `oeuvres.js` | **Le contenu** : toutes les œuvres + les textes de l'interface (FR/EN) |
| `index.html` | Accueil : héro, citation, grille de la collection |
| `oeuvre.html` | Page d'une œuvre (mur de musée + cartel + textes), via `oeuvre.html?id=...` |
| `presentation.html` | Page À propos |
| `style.css` | Tout le design |

## Fonctionnalités

- Bilingue FR / EN (choix mémorisé)
- Grille de collection générée automatiquement, avec cartels façon musée
- Page œuvre : présentation « mur de galerie » avec passe-partout et cartel, onglets *Mon regard* / *Histoire & contexte*, navigation entre œuvres, plein écran
- Responsive (mobile → grand écran), animations respectant `prefers-reduced-motion`
