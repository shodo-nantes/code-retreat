---
title: 📦 No Primitives
tags:
  - constraint
  - constraint/code
---

# No Primitives / Pas de primitive

## Niveau 1 🌶️

Toute méthode (autres que les constructeurs) ne doit accepter que des classes comme argument et pas de primitive.

Les nombres, les chaînes de caractères, etc. ne sont pas autorisés, même en utilisant les "classes primitives" de Java (
Integer, Boolean, String, etc.).

## Niveau 2 🌶️🌶️

Aucune fonction ne doit renvoyer de valeur primitive, pas même les lambdas