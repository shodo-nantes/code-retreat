---
title: 🔇 Silent Pair-Programming
tags:
  - constraint
  - constraint/human
---

# Silent Pair-Programming

> Contrainte spécifique au [Pair-Programming].
> Pour le [Mob-Programming], allez plutôt voir le [Mute Mobbers]

Aucune communication verbale n'est autorisée entre les deux particpans du binôme pendant toute la durée de l'exercice :

- pas de discussion à voix haute,
- pas d'explication orale,
- pas de débat sur les choix techniques.

Seul le code peut être utilisé pour communiquer : des noms de variables explicites, des tests clairs, des
refactorings progressifs, mais il est interdit d’utiliser les commentaires de code à cet effet.

!!! idea "Conseil"

    En tant que Driver, essayez de vous exprimer au travers du code, en respectant les trois niveaux Intention/Emplacement/Détail 
    afin que votre partenaire puisse suivre votre raisonnement.
 
    Echangez fréquemment vos rôles pour converger plus rapidement.

👉🏻 Cette contrainte force à écrire du code auto-explicatif, à privilégier de très petites étapes incrémentales
compréhensibles sans explication, et à développer une intention de code cristalline.

Elle révèle rapidement les zones de
code obscures ou ambiguës et encourage une discipline rigoureuse où chaque transformation doit être évidente pour le
binôme sans nécessiter de justification verbale.

{% include-markdown "../.links.md" %}.