---
title: (λ) Everything is a function
tags:
  - constraint
  - constraint/code
---

# (λ) Everything is a function

La contrainte de kata de code "Everything is a function" ("Tout est une fonction") consiste à écrire un programme dans
un style de programmation purement fonctionnel où toute logique doit être exprimée sous forme de fonctions pures.

Vous devez considérer toutes les valeurs et opérations comme des fonctions, en transformant les éléments statiques comme
les variables et les structures de contrôle traditionnelles en fonctions pures et en utilisant des expressions
fonctionnelles et des compositions de fonctions.

Vous devez privilégier l'immutabilité, la récursion, et les fonctions d'ordre supérieur (map, filter, reduce, etc.).
Chaque fonction doit retourner une nouvelle valeur sans modifier ses paramètres d'entrée ni l'état global. Par exemple,
au lieu de modifier un tableau avec une boucle, vous devriez transformer les données avec map ou reduce.