---
title: 📦 No Primitives
tags:
  - constraint
  - constraint/code
---

# 📦 No Primitives / Pas de primitive

**Il est interdit d'utiliser directement les types primitifs de votre langage** (int, string, boolean, float, etc.)
**ou leurs équivalents objets** (Integer, String, etc.).

Vous ne pouvez pas non plus utiliser directement les tableaux, les listes, ou les dictionnaires.

Chaque donnée ayant une signification dans votre domaine et vos concepts métiers, doivent être représentés par un type
dédié. Toutes vos fonctions ne devraient accepter que des types définis par votre domaine métier, et aucun argument de
type primitif. 

Exception faite des constructeurs, qui acceptent des types primitifs.

!!! idea "Conseil"

    Ne lésinez pas sur les "Value Object" et les "First-Class Collection". 

👉🏻 Cette contrainte force à enrichir le modèle de domaine en créant un vocabulaire explicite et en centralisant les règles
de validation au plus près des données concernées. Les primitifs ne sont autorisés qu'à l'intérieur de ces classes
d'encapsulation, jamais exposés directement dans les signatures de méthodes ou comme attributs de classes métier.


## Aller plus loin

Aucune fonction ne doit renvoyer de type primitif, pas même les lambdas, ou les fonctions anonymes.