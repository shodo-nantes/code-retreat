---
title: ✍️ Coder < Prompter
tags:
  - constraint
  - constraint/human
---

# ✍️ Coder < Prompter

> Contrainte spécifique au [Pair-Programming].

Vous ne codez pas votre propre idée : vous **écrivez une intention** que votre partenaire implémente.

Déroulé :

1. A écrit un `TODO` dans le code : une description claire de ce qu'il faut faire (le « prompt »). Il n'écrit pas l'implémentation.
2. B implémente ce `TODO` (et le supprime une fois fait).
3. B écrit à son tour un `TODO` pour l'étape suivante.
4. A l'implémente, et ainsi de suite.

!!! experiment "Exemple"

    ```
    // TODO: une cellule vivante avec moins de 2 voisines vivantes doit mourir à la génération suivante
    ```

Le `TODO` doit être assez précis pour être compris sans explication orale, mais ne doit pas dicter le code à écrire.

!!! idea "Conseil"

    Gardez des `TODO` petits : un seul comportement à la fois. Cette contrainte s'accorde bien avec le [TDD] : un `TODO` peut être « écrire le test qui... ».

👉🏻 Cette contrainte met l'accent sur la formulation de l'intention et sur la compréhension de celle des autres, à la manière d'un échange avec un assistant de code, mais entre humains.

{% include-markdown "../.links.md" %}
