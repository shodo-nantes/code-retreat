# Outside-In TDD


L'Outside-In TDD est une approche du Test-Driven Development (TDD) 
qui consiste commencer par écrire les tests matérialisant les interactions du système avec l'extérieur,
puis à rentrer peu à peu dans le système, cyle de TDD après cycle du TDD.

Exemples :

- Pour une application Web, cela consisterait à commencer par écrire les tests bout en bout (end-to-end, e2e)
- Pour une API, cela consisterait à commencer par écrire les tests du controller Web
- Pour le Game Of Life, cela consisterait à commencer par écrire des tests d'affichage du jeu, ou d'interaction avec celui-ci