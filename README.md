# Shodo Code Retreats

Chez Shodo cela nous arrive de faire des "Code Retreat".
Ce repository existe pour fournir un support avec des katas, des contraintes, des conseils de facilitation et un
historique des Code Retreat passées.

# Démarrer en local

Ce site statique utilise

- [MkDocs](https://www.mkdocs.org/) pour générer du HTML à partir de Markdown.
- [RevealJS](https://revealjs.com/) pour utiliser le Makdown comme slides de présentation

## Install

Cloner le repository, **récursivement** pour récupérer reveal.js en tant que dépendance

```shell
git clone --recurse-submodules git@github.com:shodo-nantes/code-retreat.git
```

Si vous avez oublié le côté "récursif", pas d'inquiétude, on peut se rattraper avec la commande suivante

```shell
git submodule update --init --recursive

# Option #2 : supprimer le fichier .gitmodules et saisir la commande suivante
# git submodule add https://github.com/hakimel/reveal.js.git theme/reveal.js
```

## Install MKDocs

Installer MkDocs et les plugins nécessaires à la génération du site statique

- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)

```shell
# Le fichier requirements contient les modules python à ajouter à mkdocs
pip install -r theme/requirements.txt 
```

Démarrer un serveur local pour générer et afficher le site en continu

```shell
mkdocs serve
```

# Deployer le site

Le site est mis à disposition par le mécanisme de GitHub Pages.
Un déploiement continu est configuré avec GitHub Actions, pour générer le site depuis la branche `main` et pusher le
contenu généré sur une branche `gh-branch`.
Puis, Github utilise le html présent cette dernière pour servir le site statique.