---
title: 🏓 Ping-Pong
tags:
  - constraint
  - constraint/human
---

# Ping-Pong Pair-Programming

> Contrainte spécifique au [Pair-Programming]

Le binômage dit ping-pong permet de coupler la pratique du binômage avec le [TDD].
Dans ce cadre, les itérations ne sont plus rythmées par le temps, mais par le cycle du [TDD].
Les rôles alternent à chaque fois qu’on termine une phase rouge du cycle de [TDD].

Exemple : Alice et Bertrand binôment.

➡️ _Alice est Driver, Bertrand est Nagivator_

1. Alice écrit un premier test en échec et **passe la main à Bertrand**.

      ➡️ _Les rôles alternent : Alice devient Nagivator, Bertrand devient Driver_

2. Bertrand corrige le test.
3. Bertrand effectue les refactorings nécessaires.
4. Bertrand écrit un nouveau test en échec et **passe la main à Alice**.

      ➡️ _Les rôles alternent : Alice devient Driver, Bertrand devient Nagivator_

6. Alice corrige le test.
7. Alice effectue les refactorings nécessaires.
8. Le cycle recommence à partir du point 1
 
{% include-markdown "../.links.md" %}.