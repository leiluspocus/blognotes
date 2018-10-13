---
id: 179
title: Débuter avec Sails
date: 2016-05-08T19:38:05+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=179
permalink: /fr/debuter-avec-sails/
categories:
  - HackDays
tags:
  - javascript
  - node.js
  - sails
---
Après mon HackDay sur Node.js, j&rsquo;ai eu quelques inquiétudes sur mes aptitudes à rapidement faire n&rsquo;importe quoi au niveau de la structure de mon application.

Je me suis donc mise à la recherche d&rsquo;un framework sympa qui pourrait m&rsquo;aider à mieux structurer mon application Node.js : après une petite recherche, je suis tombée sur Sails et Meteor (qui fera aussi l&rsquo;objet d&rsquo;un HackDayz !).

Voici mon petit retour de ces quelques heures de bachotages.

## Facile à appréhender

Pour les habitués de framework MVC, Sails nous permet de nous y retrouver facilement avec son architecture bien rodée. Les routes se créent simplement à partir du fichier config/routes.js

Le framework utilise Express que j&rsquo;avais déjà appréhendé lors de mon premier tutoriel Node.js

On peut demander à une route dans ce fichier de retourner directement un template ou de passer par un contrôleur qui lui rendra le template.

Des commandes permettent de générer directement les fichiers contrôleurs / modèles (ça m&rsquo;a rappelé de bons souvenirs de Ruby ça).

<pre class="EnlighterJSRAW" data-enlighter-language="shell">sails generate api &lt;nom_resource&gt;</pre>

Il est aussi possible de générer un modèle séparement et définir les données qu&rsquo;il contient.

On démarre ensuite l&rsquo;application avec un sails lift. Et on savoure le beau ASCII art de début \o/

[<img class="alignnone size-thumbnail wp-image-184" src="http://latrmouh.org/blog/wp-content/uploads/2016/05/Capture-d’écran-2016-05-08-à-7.36.25-PM-150x150.png" alt="Capture d’écran 2016-05-08 à 7.36.25 PM" width="150" height="150" />](http://latrmouh.org/blog/wp-content/uploads/2016/05/Capture-d’écran-2016-05-08-à-7.36.25-PM.png)

Un petit aperçu de ce que j&rsquo;ai pu produire de ce HackDay : [une petite application qui permet de partager des messages secrets](https://github.com/leiluspocus/shredder). Je la pousserai prochainement sur Heroku 🙂

## Deploy friendly

Le framework vient avec un système bien pratique pour gérer différents environnements (dev, staging, prod par exemple). Il suffit de définir les variables qui changent selon l&rsquo;environnement dans le dossier

<pre>config/env/</pre>

## Quelques liens sympas

[Documentation Sails](http://sailsjs.org/documentation/concepts/services/creating-a-service)

[Comment déployer une app Sails sur Heroku](http://stackoverflow.com/questions/16205028/deploying-a-sails-js-app-to-heroku)

&nbsp;

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->