---
id: 181
title: Débuter avec Mongo DB
date: 2016-11-10T09:01:20+00:00
author: leiluspocus
excerpt: "Une cheatsheet des commandes dont j'ai eu besoin lorsque j'ai débuté avec MongoDB."
layout: post
guid: http://latrmouh.org/blog/?p=181
permalink: /fr/debuter-avec-mongo-db/
categories:
  - HackDays
tags:
  - cheat sheet
  - mongo
---
## Démarrer Mongo

<pre class="EnlighterJSRAW" data-enlighter-language="shell">mongod</pre>

## Démarrer Mongo sans les journaux

<pre class="EnlighterJSRAW" data-enlighter-language="null">mongod --nojournal</pre>

Peut être pratique si vous n&rsquo;avez pas beaucoup d&rsquo;espace sur votre ordi.

## Se connecter en Shell à Mongo

<pre class="EnlighterJSRAW" data-enlighter-language="shell">mongo</pre>

&nbsp;

## Créer une base de données

<pre class="EnlighterJSRAW" data-enlighter-language="shell">use &lt;nom_de_la_base_de_données&gt;</pre>

Il faut y enregistrer au moins un document pour que la base de données soit vraiment sauvegardée.

## Créer un utilisateur

<pre class="EnlighterJSRAW" data-enlighter-language="shell">db.createUser(
{
  user: "fashion",
  pwd: "fashion",
  roles: [ "readWrite", "dbAdmin" ]
});</pre>

## Voir le contenu d&rsquo;une collection

<pre class="EnlighterJSRAW" data-enlighter-language="shell">db.&lt;nom_collection&gt;.find();</pre>

_Une collection Mongo s&rsquo;apparente à une table MySQL et un document Mongo s&rsquo;apparente à l&rsquo;entrée d&rsquo;une table MySQL. _

&nbsp;

show all content collection: http://stackoverflow.com/questions/24985684/mongodb-show-all-contents-from-all-collections

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->