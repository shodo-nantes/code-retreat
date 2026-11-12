---
title: 📖 DocAsTest
tags:
  - constraint
  - constraint/code
---

# 📖 DocAsTest

> 🔗 https://sfauvel.github.io/documentationtesting/

**DocAsTest** est une démarche (et un framework) de [Sébastien Fauvel](https://github.com/sfauvel) qui vise à **définir le comportement en un seul endroit : le code**.
La documentation n'est pas écrite à la main : elle est **générée par les tests**. Elle sert ensuite de référence pour détecter les régressions.

La démarche mélange trois pratiques :

- la **documentation vivante** : elle est produite par des artefacts exécutables, donc toujours à jour,
- le **Golden Master** (test de caractérisation) : on garde une trace du comportement réel du système,
- le **BDD** : le comportement est exprimé par des scénarios lisibles par tout le monde.

## Le principe

Un test classique est difficile à lire pour quelqu'un qui ne code pas :

```java
@Test
public void player_A_won_1_point_and_then_player_B_win_2_points() {
    game.pointA();
    game.pointB();
    game.pointB();
    assertEquals("15-30", game.score());
}
```

Avec DocAsTest, ce même test **produit un document** lisible par toute l'équipe, par exemple un tableau de score de tennis :
les points gagnés par chaque joueur, et le score obtenu (15-30).

Le scénario qu'on lit et le test qui s'exécute sont **le même artefact** :

1. le test exécute le code et **génère** la documentation (le résultat « reçu »),
2. ce résultat est **comparé** à la version précédemment validée (le résultat « approuvé »), comme dans l'*approval testing*,
3. si le comportement change, la comparaison échoue : on relit la différence et, si elle est voulue, on **approuve** la nouvelle documentation.

## La contrainte

Pendant l'itération, vous ne vérifiez pas votre code avec des assertions classiques :
**chaque comportement doit être documenté par un document généré par un test**, que quelqu'un qui ne code pas pourrait lire.

- vous décidez à quoi doit ressembler la documentation (phrases, tableaux, scénarios) **avant** d'écrire le code,
- le test génère ce document et le compare à la version approuvée,
- vous n'approuvez un changement qu'après avoir relu le document et vérifié qu'il décrit bien le comportement voulu.

!!! experiment "Exemple avec Game Of Life"

    Le test génère le document suivant, que l'on relit puis approuve :

    ```
    Une cellule vivante avec moins de 2 voisines vivantes meurt.

    | Cellule | Voisines vivantes | Prochaine génération |
    |---------|-------------------|----------------------|
    | vivante | 0                 | morte                |
    | vivante | 1                 | morte                |
    | vivante | 2                 | vivante              |
    ```

!!! idea "Conseil"

    Il existe des implémentations du framework en [Java](https://sfauvel.github.io/documentationtesting/) et en Python (`doc_as_test_pytest`).
    Dans un autre langage, un outil d'*approval testing* (ex : ApprovalTests) suffit : le principe est de générer un texte lisible, puis de le comparer à une version approuvée.

👉🏻 Cette contrainte force à exprimer l'**intention métier** dans des termes compréhensibles par tous, et fait de la documentation un résultat du développement plutôt qu'une tâche à part.

{% include-markdown "../.links.md" %}
