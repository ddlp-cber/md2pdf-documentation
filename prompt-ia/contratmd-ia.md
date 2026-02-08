# Markdown to PDF – Contract de formatage

## Objectif

Ce document définit les règles de production du Markdown destiné à être converti automatiquement en PDF.

Le non-respect de ces règles entraîne un rendu incorrect.

## Règles générales

- Markdown CommonMark strict
- Pas de HTML brut
- Pas de CSS inline
- Une seule structure logique par document

## Structure du document

### Titre principal

- Un seul `#`
- Placé en première ligne
- Sert de titre de document et de page de garde

### Hiérarchie des titres

- `#` : titre du document
- `##` : sections principales (nouvelle page)
- `###` : sous-sections
- Interdiction d’aller au-delà de `####`

### Numérotation des titres

- Le Markdown produit ne doit contenir aucune numérotation manuelle dans les titres.
- Les titres doivent être rédigés sans préfixe numérique.
- Toute numérotation éventuelle est gérée séparément.

## Sauts de page

- Chaque titre `##` (section principale) doit être précédé d'un saut de page explicite
- Syntaxe du saut de pages : une ligne avec seulement `---`
- Le saut de page `---` doit être inséré immédiatement avant chaque titre `##` (sauf le premier titre `##` qui suit directement le titre principal `#`)
- Aucun autre saut de page manuel n'est autorisé ailleurs dans le document

## Métadonnées et cartouches techniques

### Principe général

- Les métadonnées (notes de version, auteur, date, identifiant interne, commentaires techniques)
- ne doivent jamais être interprétées comme des titres ou du contenu documentaire.

### Règle obligatoire

- Tout cartouche d’en-tête ou note technique doit être placé dans un bloc de code Markdown.
- Aucun caractère `#` ne doit apparaître en dehors d’un bloc de code pour des métadonnées.

## Sommaire

- Pas de section nommée “Sommaire” dans le contenu

## Diagrammes

### Mermaid

- Utiliser uniquement des blocs :

````

```mermaid
...
````

- Un diagramme par bloc
- Toujours précédé d’un titre `###`

## Listes
- Listes plates uniquement
- Pas d’imbrication au-delà d’un niveau

## Tableaux
- Markdown pipe standard
- Pas de cellules fusionnées
- Largeur contrôlée par le moteur PDF, pas par l’IA

## Encadrés sémantiques
Utiliser les conventions suivantes :

> **Note**
> Texte…

> **Attention**
> Texte…

> **Exemple**
> Texte…

## Interdictions formelles
- Pas d’emojis
- Pas de liens nus
- Pas de références externes non explicites
- Pas de blocs de code (fences) préfixés par `>` (pas de code dans les blockquotes)
