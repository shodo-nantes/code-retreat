---
title: 🎯 Only one Decision at a Time
tags:
  - constraint
  - constraint/code
---

# 🎯 Only one Decision at a Time

> 🔗 https://philippe.bourgau.net/a-slow-code-retreat-to-be-less-in-a-hurry/#slow-todo-list

À chaque instant, vous ne prenez **qu'une seule décision** de conception ou d'implémentation.
Dès qu'une seconde décision apparaît, vous ne la traitez pas : vous la notez, et vous finissez la première.

Pour cela, nous utilisons la méthode **Slow TODO list**, issue du *Slow Code Retreat* de Philippe Bourgau :
prendre le temps de se concentrer uniquement sur la tâche en cours, en s'appuyant sur une liste de choses à faire.

Une décision peut être, par exemple :

- choisir le nom d'une classe ou d'une méthode,
- choisir où placer une responsabilité,
- choisir une structure de données,
- choisir le prochain comportement à tester.

## La méthode : la Slow TODO list

Pendant tout l'exercice, vous tenez une liste TODO **visible par les deux membres du binôme**.

1. **Démarrez la liste** avec la tâche en cours.
2. **Notez tout ce qui reste à faire**, dès que vous y pensez (étapes à venir, idées, décisions en attente, doutes).
3. **Ne traitez qu'un seul élément à la fois** : celui sur lequel vous travaillez maintenant.
4. **Cochez ou barrez** chaque étape terminée.
5. **Décomposez** les éléments complexes en sous-tâches, indentées sous l'élément concerné.
6. **Réorganisez** la liste dès que votre compréhension évolue : c'est normal, pas un échec.
7. **Supprimez volontairement** les éléments que vous décidez finalement de ne pas faire.

!!! experiment "Exemple"

    ```
    - [x] Une cellule vivante avec moins de 2 voisines meurt
    - [ ] Une cellule vivante avec 2 ou 3 voisines survit   <- en cours
        - [ ] Nommer la méthode qui compte les voisines
        - [ ] Choisir la représentation d'une cellule
    - [ ] Une cellule morte avec 3 voisines naît
    - [ ] Gérer les bords de la grille
    ```

    En cours de route, vous hésitez sur la représentation d'une cellule alors que vous cherchez un nom de méthode :
    vous tranchez d'abord le nom, et « représentation d'une cellule » reste dans la liste pour plus tard.

!!! idea "Conseil"

    Gardez l'outil simple : un fichier `.txt` ou Markdown, un document partagé ou une mind map suffisent.
    L'important est que la liste soit à jour et lisible par votre binôme.

    Si vous annulez (`revert`) vos changements parce qu'une étape est impossible tant qu'une autre n'est pas faite,
    gardez l'étape bloquée dans la liste et travaillez d'abord sur ses prérequis : vous pratiquez alors la méthode Mikado.

    Cette contrainte se marie très bien avec [Nommer les classes avec des verbes](../verb-class-names/index.md) : choisir un verbe est une décision à part entière.

👉🏻 Cette contrainte **allège la charge mentale** (l'état du travail n'est plus dans votre tête), sert d'**outil de communication** dans le binôme,
rend les décisions **conscientes et explicites**, et vous aide à rester dans de [petits pas](../baby-steps/index.md).

{% include-markdown "../.links.md" %}
