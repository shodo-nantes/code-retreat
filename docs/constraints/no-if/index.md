---
title: ⛔ No if
tags:
  - constraint
  - constraint/code
---

# ⛔ No if / Pas de "if"

Il est interdit d'utiliser toute forme de structure conditionnelle explicite : `if`, `else`, `else if`, `switch` /
`case`, l'opérateur ternaire `? :`, ou toute autre instruction de branchement conditionnel.

Faites preuve de créativité pour repenser votre conception en exploitant en utilisant d’autres mécanismes à votre
disposition tels que le polymorphisme, les design patterns (Strategy, State, Command, etc.), les structures de données
(dictionnaires/maps pour remplacer les switch).

Les méthodes de collections qui utilisent des instructions conditionnelles sont à éviter également (filter, find, etc.).

!!! experiment "Exemple"

    🚫 Evitez
    ```
    if (type == "A") {
        doA(); 
    } else {
        doB(); 
    }
    ```
    ✅ Privilégiez: de créer des classes distinctes avec une interface commune et déléguer le comportement approprié.

👉🏻 Cette règle encourage à écrire du code plus orienté objet, plus extensible et respectueux du principe Open/Closed, tout
en rendant les variations de comportement explicites dans la structure même du code plutôt que cachées dans des
conditions.

N'hésitez pas à faire appel aux facilitateur·ices pour avancer sur cette contrainte.