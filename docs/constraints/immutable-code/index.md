---
title: 🪨 Immutable Code
tags:
  - constraint
  - constraint/code
---

# 🪨 Immutable Code

Pour ce kata, vous devez respecter le principe d'immutabilité stricte.

**Aucun objet ne peut être modifié après sa création**

Il est interdit de modifier l'état d'un objet, d'une structure de données ou d'une variable après sa
création.

**Aucune variable ne peut être réassignée.**

Toute variable doit être déclarée comme constante (const, final, readonly, etc.) et ne peut être assignée qu'une seule
fois.

**Aucune liste ou collection ne peut être enrichie ou filtrée après sa création.**

Les collections (listes, tableaux, dictionnaires) ne peuvent pas être modifiées après leur initialisation : pas de
add(), remove(), push() ou modification d'index.

!!! idea "Conseil"

    Au lieu de muter des données existantes, vous devez créer de nouvelles instances avec les modifications souhaitées.
    Par exemple, pour "modifier" un objet Person, vous devriez créer un nouveau Person avec les nouvelles valeurs plutôt
    que d'utiliser des setters.

👉🏻 Cette contrainte élimine les effets de bord, rend le code plus prévisible et facilite le raisonnement sur le flux de
données. Elle encourage l'utilisation de méthodes retournant de nouvelles copies transformées (comme map, filter) et
l'adoption de patterns comme le Builder pour construire des objets complexes de manière lisible.