---
title: 🧮 String Calculator
---

# 🧮 String Calculator

![](../../assets/images/katas/string-calculator/pac-man-screen.webp)

> Bootstrap : <br>
> 🔗 https://github.com/shodo-nantes/kata-starters

Créez simplement une calculatrice comme celle que vous utilisiez à l'école.

## Gérer des opérations simples unitaires

- Créez une calculatrice String simple avec une méthode `calculate` qui accepte une chaine de caractère en argument et qui renvoie une chaine de caractères.
  - La méthode peut prendre deux nombres séparés par "+", et retourner leur somme.
- Permettez à la méthode de gérer n'importe quelle quantité de nombres et d'opérations "+".
- Permettez à la méthode de gérer l'opération de soustraction.
- Permettez à la méthode de gérer l'opération de multiplication.

## Gérer plusieurs opérations

Permettez à la méthode de composer les différents types d'opérations. 
Gardez à l'esprit la priorité des différentes opérations.

## Gérer des opérations successives

- Permettez à la méthode de gérer deux lots d'opérations séparés par un espace.
- Exemple :
    - `1 2` retournera `1 2`
    - `1+2 3+4` retournera `3 7`

## Gérer une nouvelle opération

- Permettez à la méthode de gérer l'opération "^", qui retourne "premier exposant second".

## L'opération "x"

- Permettez à la méthode de gérer l'opération "x", qui effectue la multiplication.

## De l'aléatoire partout

- Permettez à la méthode de prendre en charge les lancers de dés :
    - 1d4 retourne un entier entre 1 et 4
    - 1d6 retourne un entier entre 1 et 6
    - Il est possible de lancer plusieurs dés.

## Gérer les parenthèses

- Permettez à la méthode de gérer "(" et ")" pour modifier les priorités d'opérations.

## Gérer les chiffres romains

- Permettez à la méthode de gérer les chiffres romains.
    - Ex : "1+I" doit retourner 2, et "2*V" doit retourner 10.
- Permettez à la méthode de gérer les chiffres romains minuscules (ex : "i", "v", etc.).
## 🔗 Ressources

* https://www.codurance.com/katas/string-calculator
* https://kata-log.rocks/string-calculator-kata