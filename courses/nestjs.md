<img src="https://raw.githubusercontent.com/millehorde/nodejs-course/master/subjects/img/logonest.svg" width=700>

---

## Histoire

Kamil MYSLIWIEC (@kammysliwiec) **2017**

Dev front -> framework backend en node.js 😱

----

<img src="https://raw.githubusercontent.com/millehorde/nodejs-course/master/subjects/img/troll.gif" width=300>
<img src="https://raw.githubusercontent.com/millehorde/nodejs-course/master/subjects/img/withKamil.jpg" width=300>

---

## Aujourd'hui

- plus de 22 800 stars sur Github
- 99 contributeurs
- Près de 2616 issues dont seulement 75 encore ouvertes
- Déjà en version 7.0.11 !
- Compatibilité TS & JS

----

<img src="https://raw.githubusercontent.com/millehorde/nodejs-course/master/subjects/img/tenor.gif" width=450>

---

## Installation

**Node.js(>= 8.9.0)**

----

To get started, avec le Nest CLI:

```bash
$ npm i -g @nestjs/cli
$ nest new project-name
```

----

Ou

```bash
$ git clone https://github.com/nestjs/typescript-starter.git project
$ cd project
$ npm install
$ npm run start
```

----

Ou encore avec NPM ou yarn:

```bash
$ npm i --save @nestjs/core @nestjs/common rxjs reflect-metadata
```

---

### Nest CLI

[Documentation](https://docs.nestjs.com/cli/usages)

`nest -h` =>

```bash
Options:

  -V, --version                                            output the version number
  -h, --help                                               output usage information

Commands:

  new|n [options] [name] [description] [version] [author]  Generate a new Nest application.
  generate|g [options] <schematic> <name> [path]           Generate a Nest element.
  info|i                                                   Display Nest CLI details
  update|u [options]                                       Update @nestjs dependencies.
  add <library>                                            Allow user to add a library
```

`<schematic>` => application, module, controller, service, pipe, interceptor, ...

---

## Architecture

Nest est né pour résoudre un problème

L'absence d'architecture complète et abstraite pour créer une application node.js

**Solution :**

Une architecture prête à l'emploi pour créer des applications hautement testables, évolutives, couplées de manière peu dépandantes (lâches) et faciles à maintenir

---

### Principe

Tout est interface !

Chaque option, chaque méthode, chaque classe est typée => meilleur maintenabilité et lisibilité (si usage de TS 😉)

----

Si installation avec CLI =>

```
- src
  - app.controller.ts // Définition des routes du AppModule (basic controller)
  - app.module.ts // Définition de AppModule, le module root de l'application
  - main.ts // Le fichier d'entrée de l'application (NestFactory)
```
----

Par convention, 1 module = 1 répertoire avec ses tests ses sous-modules

<img src="https://raw.githubusercontent.com/millehorde/nodejs-course/master/subjects/img/exemplearchi.png" width=150>

----

NestJs => Lego de module (comme node ;) )

<img src="https://raw.githubusercontent.com/millehorde/nodejs-course/master/subjects/img/batmanlego.gif" width=300>

---

## Composants

<img src="https://raw.githubusercontent.com/millehorde/nodejs-course/master/subjects/img/heart.gif" width=300>

Documentation => [ici](https://docs.nestjs.com/)

---

## Projet 👼

2 projets => 1 seul à choix qui sera définitif

----

1 niveau starter => pour les personnes ayant fait peu de JS/TS

----

1 niveau expert => pour les personnes ayant déjà fait du JS/TS et familier avec Node

----

### Niveau "Starter"

Réalisation d'une API connectée à une base PostgreSQL ou MongoDB qui mettra à disposition un CRUD complet et documenté

Elle devra gérer des boites de pokemon d'un dresseur:

----

- on peut avoir x boites
- chaque boite appartient à un dresseur (humains)
- chaque boite peut contenir un maximum de 24 pokemons
- chaque boite ne peut avoir des pokemons de maximum 2 types différents

----

- on peut supprimer une boite vide si elle nous appartient
- on peut en ajouter
- on peut deplacer/ajouter des pokemons dans une boite

----

Vous êtes libre quant aux informations contenues dans chacunes des entités mais les contraintes doivent être respectées

Pas besoin de gestion de connexion/inscription d'utilisateur

Vous utiliserez TypeOrm (pour PostgreSQL) ou Mongoose (pour MongoDB) comme ORM de votre API

----

### Niveau "Expert"

Meme travail que précédemment mais avec ajout d'une brique de gestion de dresseur

- un dresseur doit pouvoir s'inscrire/s'identifier
- il doit pouvoir ajouter/relacher/changer le pseudo d'un de SES pokemons
- visualiser ses pokemons et voir dans quel boites ils sont presents

---

### Contraintes pour les projets

API REST !

Tout code écrit doit être tester unitairement.

Vos modules doivent être tester en mode end to end (e2e).

Vous mettrez en place une documentation claire et soignée.

Vous devrez créer un repository par projet et m'identifier en tant que contributeur (@millehorde)
