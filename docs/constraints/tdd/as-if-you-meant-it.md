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

Cette approche radicalise le Test-Driven Development en imposant des règles extrêmement contraignantes :

1. vous ne pouvez écrire du code de production que dans les tests initialement,
2. vous ne pouvez créer une nouvelle méthode qu'en extrayant du code existant dans les tests via un refactoring,
3. vous ne pouvez créer une nouvelle classe qu'en extrayant une méthode existante, et
4. chaque étape doit être la plus petite transformation possible tout en gardant les tests au vert.

Concrètement,

1. vous commencez par écrire tout votre code directement dans la méthode de test,
2. vous refactorez progressivement votre code en extrayant des méthodes dans la classe de test,
3. vous refactorez progressivement votre code en déplaçant vos méthodes de la classe de test vers des nouvelles classes lorsquele besoin devient évident.

Keith Braithwaite propose la procédure suivante :

1. Écrivez un nouveau test qui vous rapproche de la solution
2. Constatez que le test échoue
3. Faites passer le test de \#1 en écrivant le moins de code possible, et uniquement **dans la méthode de test**.
4. Refactorez pour supprimer les doublons et, si nécessaire, pour améliorer la conception.
   Soyez intransigeant sur les règles suivantes :
    1. Vous voulez une nouvelle méthode ? attendez l'étape de réfactor, puis... créez de nouvelles méthodes en suivant
       **uniquement** ceci :
        1. Utilisez votre IDE pour faire une **extraction de méthode** dans la classe de test
        2. Si vous n'avez pas d'autres solutions : déplacez manuellement le code implémenté en \#3 vers une méthode
           existante.
    2. Vous voulez une nouvelle classe ? attendez l'étape de réfactor, puis... utilisez votre IDE pour déplacer des
       méthodes existantes vers une classe que vous créez à la volée.
        - Alimentez vos classes uniquement en déplaçant des méthodes avec votre IDE

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

// Ensuite : déplacer votre classe ou fonction dans le bon package (éventuellement dans le code de prod)

// Second test

@Test
public void fizzbuzz_of_3_displays_Fizz() {
	assertThat((3 == 3) ? "Fizz" : "3").isEqualTo("Fizz");
}

// Refactor

@Test
public void fizzbuzz_of_3_displays_Fizz() {
	assertThat(new FizzBuzz().displayFizzBuzzOfThree()).isEqualTo("Fizz");
}

class FizzBuzz {
	String displayFizzBuzzOfOne() {
		return String.valueOf(1);
	}

	String displayFizzBuzzOfThree() {
		return (3 == 3) ? "Fizz" : "3";
	}
}

// Et... j'espère que vous avez mieux refactoré que moi le premier test, afin de pouvoir combiner les deux méthodes :-)
```

👉🏻 Cette contrainte force une conception émergente pure, guidée exclusivement par les tests,
et empêche toute anticipation ou sur-ingénierie en vous obligeant à découvrir l'architecture au fur et à mesure.

## 🔗 Ressources

- ["TDD as if you meant it" par Keith Braithwaite](https://web.archive.org/web/20240130003458/https://cumulative-hypotheses.org/2011/08/30/tdd-as-if-you-meant-it/)
