---
title: 📦 No Primitives
tags:
  - constraint
  - constraint/code
---

# No Primitives / Pas de primitive

Il est interdit d'utiliser directement les types de base de votre langage, tels que les entiers, les flottants, 
les booléens, les chaînes de caractères, etc. Vous ne pouvez pas non plus utiliser directement les tableaux, les listes,
ou les dictionnaires.

Pour manipuler ces types primitifs, vous devrez modéliser votre métier, créer vos propres types personnalisés, 
et encapsuler les types primitifs dans vos types personnalisés.

Aucune fonction ne peut accepter de type primitive, à l'exception des constructeurs.
Tous les arguments de vos fonctions sont nécessairement des types personnalisés.

> 💡Conseil
>
> Ne lésinez pas sur les "Value Object" et les "First-Class Collection". 

## Aller plus loin

Aucune fonction ne doit renvoyer de type primitif, pas même les lambdas