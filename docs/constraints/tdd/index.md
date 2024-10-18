---
title: "🚥 TDD : Test Driven Development"
tags:
  - constraint
  - constraint/code
---

# Test-Driven Development (TDD)

Le Test-Driven Development (TDD) est une méthodologie de développement par une refactorisation continue, qui consiste à
écrire les tests unitaires autorisant la refactorisation, avant d'écrire le code de production à refactoriser.

## Cycle du TDD

Le TDD propose trois étapes principales

### Red

> Make it fail

Faites échouer votre code !

Écrire un test unitaire et l'exécuter pour s'assurer qu'il échoue.

Le test que l'on écrit définit une fonctionnalité ou une amélioration qui n'existe pas encore.
Le code lui-même n'existe pas, et on peut se retrouver à avoir des erreurs de compilation (dans le cas des languages
compilés), ou utiliser des structures ou des fonctions inexistantes, mais désirées.

### Green

> Make it pass

Faites fonctionner votre code !

Écrire le code le plus simple possible, permettant de faire passer le test.

Tous les coups sont permis, que ce soit d'écrire des valeurs en dur, d'implémenter une solution partielle ou
d'implémenter une solution évidente. L'objectif étant de faire passer le test, et non pas d'implémenter la
fonctionnalité.

### Refactor

> Make it better

Faites briller votre code !

Prenez le temps de retravailler votre code à tête reposée, sans pression.
Refactorisez en améliorant la structure de votre code, sans en altérer le comportement : vous avez des tests qui le
garantissent.

Prenez également le temps de refactoriser vos tests unitaires. Plus vous faites des étapes petites, plus vous aurez
des "micro-test" (en effet de bord), qui n'ont pas vocation à survivre au développement.

Choisissez les tests unitaires que vous voulez garder.

## Les trois règles du TDD

Une personne influence a décrit le TDD en trois règles :

1. You are not allowed to write any production code unless it is to make a failing unit test pass.
2. You are not allowed to write any more of a unit test than is sufficient to fail; and compilation failures are failures.
3. You are not allowed to write any more production code than is sufficient to pass the one failing unit test.

Ce que nous comprenons de la façon suivante

### Permis de coder

> You are not allowed to write any production code unless it is to make a failing unit test pass.

Interdit d’écrire du code, sans test en échec qui prouve que ce code est nécessaire.

Le TDD est 

### Une question à la fois

Interdit d’écrire plus d’un test en échec à la fois

### Connaître les limites

Interdit d’écrire plus de code que nécessaire, pour faire passer le test en cours.