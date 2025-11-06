---
title: TDD As If You Meant It
tags:
  - constraint
  - constraint/code
---

# TDD As If You Meant It

Le code ne doit être généré **que** dans les tests.

La seule manière de créer du code de production, est de pratiquer des opérations de refactoring comme
l'extraction de méthodes/classes/champs/variables, etc.

Pour ce kata, vous devez respecter la discipline stricte "TDD as if you meant it" créée par Keith Braithwaite. 
Cette approche radicalise le Test-Driven Development en imposant des règles extrêmement contraignantes :

1. vous ne pouvez écrire du code de production que dans les tests initialement,
2. vous ne pouvez créer une nouvelle méthode qu'en extrayant du code existant dans les tests via un refactoring, 
3. vous ne pouvez créer une nouvelle classe qu'en extrayant une méthode existante, et
4. chaque étape doit être la plus petite transformation possible tout en gardant les tests au vert.

Concrètement, vous commencez par écrire tout votre code directement dans la méthode de test, puis vous le 
refactorisez progressivement en extrayant des méthodes privées dans la classe de test, 
puis des méthodes dans de nouvelles classes uniquement quand le besoin devient évident. 

Exemple sur le FizzBuzz :

```java

// Premier test

@Test
public void fizzbuzz_of_1_displays_1() {
    assertThat(String.valueOf(1)).isEqualTo("1");
}

// Refactor: Extract method

@Test
public void fizzbuzz_of_1_displays_1() {
    assertThat(displayFizzBuzzOfOne()).isEqualTo("1"); // Éventuellement ici, vous optez pour d'autres stratégies d'implementation
}

String displayFizzBuzzOfOne() {
    return String.valueOf(1);
}


// Refactor: Extract class

@Test
public void fizzbuzz_of_1_displays_1() {
    assertThat(new FizzBuzz().displayFizzBuzzOfOne()).isEqualTo("1"); // Éventuellement ici, vous optez pour d'autres stratégies d'implementation
}

class FizzBuzz {
    String displayFizzBuzzOfOne() {
        return String.valueOf(1);
    }
}

// Then : move class in proper package (or source folder)

```

👉🏻 Cette contrainte force une conception émergente pure, guidée exclusivement par les tests, 
et empêche toute anticipation ou sur-ingénierie en vous obligeant à découvrir l'architecture au fur et à mesure.


## 🔗 Ressources
- ["TDD as if you meant it" par Keith Braithwaite](https://web.archive.org/web/20240130003458/https://cumulative-hypotheses.org/2011/08/30/tdd-as-if-you-meant-it/)
