---
title: 🏃 Classes nommées avec des verbes
tags:
  - constraint
  - constraint/code
---

# 🏃 Classes nommées avec des verbes

Toutes les classes que vous créez doivent porter un **nom de verbe** (ou de groupe verbal), et non un nom de chose :
`Calculator` devient `Calculate`, `CellNeighbours` devient `CountNeighbours`, `GameRules` devient `ApplyRules`.

Une classe n'est alors plus un « machin » qui contient des données, mais une **action** : ce que le code *fait* pour répondre à un besoin.

!!! experiment "Exemple"

    🚫 Evitez
    ```
    class NeighbourCounter { ... }
    class Generation { ... }
    ```
    ✅ Privilégiez
    ```
    class CountNeighbours { ... }
    class EvolveToNextGeneration { ... }
    ```

👉🏻 Cette contrainte oblige à se demander *ce que l'on veut faire* avant de se demander *ce que l'on manipule*.
Elle rapproche le code de l'intention humaine, et fait émerger des classes courtes, avec une seule responsabilité.

!!! idea "Conseil"

    Si vous ne trouvez pas de verbe, c'est peut-être que la classe fait trop de choses, ou qu'elle ne sert à rien.
    Discutez-en avec votre binôme : le débat sur le nom est souvent un débat sur la conception.

{% include-markdown "../.links.md" %}
