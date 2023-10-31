---
tags:
- constraint
---
# Ping-Pong Pair-Programming

> Contrainte spécifique au [Pair-Programming](index.md)

Le binômage dit ping-pong permet de coupler la pratique du binômage avec le TDD.
Dans ce cadre, les itérations ne sont plus rythmées par le temps, mais par le cycle du TDD.
Les rôles alternent à chaque fois qu’on termine une phase rouge du cycle de TDD.

Exemple : Alice et Bertrand binôment.

➡️ _Alice est pilote, Bertrand est copilote_

1. Alice écrit un premier test en échec et **passe la main à Bertrand**.

    ➡️ _Les rôles alternent : Alice devient copilote, Bertrand devient pilote_

2. Bertrand corrige le test.
3. Bertrand effectue les refactorings nécessaires.
4. Bertrand écrit un nouveau test en échec et **passe la main à Alice**.

    ➡️ _Les rôles alternent : Alice devient pilote, Bertrand devient copilote_

6. Alice corrige le test.
7. Alice effectue les refactorings nécessaires.
8. Le cycle recommence à partir du point 1.