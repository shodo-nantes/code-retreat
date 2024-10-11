---
title: 🏁 Game Of Life
---
# 🏁 Game Of Life

> Bootstrap : <br>
> 🔗 https://github.com/shodo-nantes/kata-starters

Le Jeu de la Vie de Conway est un jeu de simulation de la vie dans lequel l'état d'une cellule à un instant 
donné dépend de l'état de ses voisines à l'instant précédent.

Le jeu se déroule sur une grille à deux dimensions, théoriquement infinie, dont les cases — appelées « cellules »,
peuvent prendre deux états distincts : « vivante » ou « morte ».

L'objectif de ce kata est de réaliser un petit moteur de jeu permettant de calculer l'état de la prochaine
génération de cellules et de l'afficher dans une grille à deux dimensions.

## 🌱 Cycle de vie d'une cellule

À chaque instant, le prochain état d’une cellule est déterminée par l’état de ses huit cellules voisines au même instant, 
selon les règles suivantes :

- Toute cellule vivante ayant moins de 2 voisins vivants meurt, par sous-population.
- Toute cellule vivante ayant 2 ou 3 voisins vivants, survit à la génération suivante.
- Toute cellule vivante ayant plus de 3 voisins vivants meurt, par surpopulation.
- Toute cellule morte reste morte.
- Toute cellule morte ayant exactement 3 voisins vivants, naît par reproduction.

## 🖼️ Affichage

Vous êtes libres de choisir l'affichage que vous souhaitez pour représenter votre Jeu de la Vie.

Voici une suggestion pour représenter une grille cartésienne : 

```
Génération 1
........
....*...
...**...
........
```
```
Génération 2
........
...**...
...**...
........
```

## 🔀 Variantes

### 🧟 Zombies

Cette variante du Game of Life ajoute la règle suivante :

- Toute cellule qui meurt, puis revient à la vie, devient un zombie et ne peut plus mourir.

### 🎨 Couleurs

Les cellules vivantes sont colorées.
Lorsqu'elles prennent vie, les cellules adoptent la couleur de la majority de leurs voisins.
S'il n'y a pas de majorité, alors elles adoptent une "couleur neutre".

### Grille Hexagonale

Dans cette variante, les cellules évoluent sur une grille (infinie) hexagonale.

### 👓 Espace à trois dimensions

Dans cette variante, les cellules évoluent dans un espace à trois dimensions.
Leurs voisins ne sont plus seulement les cellules situées sur le même plan, 
mais également les 9 cellules du plan supérieur et les 9 cellules du plan inférieur.

On adapte également les règles du cycle de vie de la cellule de la manière suivantes (B4/S4)

- Toute cellule morte reste morte.
- Toute cellule morte ayant exactement 4 voisins vivants, naît par reproduction (B4)
- Toute cellule vivante ayant 4 voisins vivants, survit à la génération suivante (S4)
- Dans les autres cas, toute cellule vivante meurt, par sous-population ou par surpopulation.

<!--
### 🌱 Breeders and Seeders

Dans sa version originale, 
-->
## 🔗 Ressources

* https://conwaylife.com/book/
* https://github.com/marcoemrich/game-of-life-rules/blob/master/gol_rules.png
* https://fr.wikipedia.org/wiki/Jeu_de_la_vie
* https://www.coderetreat.org/facilitators/gameoflife/
* https://codingdojo.org/kata/GameOfLife/
