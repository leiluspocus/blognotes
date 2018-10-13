---
id: 113
title: Débuter avec Node.js
date: 2016-01-10T16:46:02+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=113
permalink: /fr/debuter-avec-node-js/
categories:
  - HackDays
tags:
  - autoformation
  - javascript
  - nodejs
---
J&rsquo;ai profité de cet après-midi pluvieux pour me familiariser avec Node.js grâce à [l&rsquo;excellent cours de Mathieu Nebra sur Open Classrooms](https://openclassrooms.com/courses/des-applications-ultra-rapides-avec-node-js).

Ce que je retiens de ces quelques heures de bachotage (pas encore poussé mon application) :

  * Javascript qui s&rsquo;exécute côté serveur
  * Force du language: la gestion d&rsquo;événements côté serveur et sa rapidité
  * NPM est un outil puissant pour la gestion des dépendances
  * Nécessite une bonne connaissance de Javascript (Closures, callbacks, prototypes).

## Quelques outils donnés sur le tutoriel bien pratiques

  * http://browsenpm.org/package.json
  
    Récapitulatif des attributs que l&rsquo;on peut préciser dans son fichier de dépendances
  * https://github.com/nodejs/node-v0.x-archive/wiki/modules#templating
  
    Modules utilisables pour le templating. J&rsquo;ai retenu juste l&rsquo;exemple de EJS donné dans le cours qui est compatible avec Express, framework Node.js
  * https://nodejs.org/api/http.html#http\_event\_close
  
    Documentation des objets utilisables dans le core de Node.js

## Bonnes pratiques de développement sous Node.js

  * https://devcenter.heroku.com/articles/node-best-practices
  * https://blog.heroku.com/archives/2015/11/10/node-habits-2016

## MongoDB x Node.js

  * http://mongodb.github.io/node-mongodb-native/2.0/overview/quickstart/
  * https://docs.mongodb.org/getting-started/node/insert/

## Quelques commandes de base

Installer un module (l&rsquo;option &#8211;save permet de rajouter le module en dépendance dans le fichier package.json)

<pre class="EnlighterJSRAW" data-enlighter-language="shell">npm install &lt;nom_du_module&gt; --save</pre>

Gestion des versions de Node

<pre class="EnlighterJSRAW" data-enlighter-language="shell"># Module n permet de gérer plus facilement le switch vers telle ou telle version de Node
sudo npm install n -g

# Se mettre sur la dernière version la plus stable de Node
sudo n stable</pre>

&nbsp;

## 

## Ce que j&rsquo;ai réalisé en Node.js

Ma première application Node.js peut-être consultée ici: https://fierce-wildwood-39907.herokuapp.com/

Le repository associé se trouve ici: https://github.com/leiluspocus/greenie

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->