---
id: 262
title: Installer une boutique Prestashop
date: 2016-11-13T11:19:27+00:00
author: leiluspocus
excerpt: "J'ai installé une boutique Prestashop from scratch dans le cadre d'un projet. Voici un petit débrief de mon expérience."
layout: post
guid: http://latrmouh.org/blog/?p=262
permalink: /fr/installer-une-boutique-prestashop/
categories:
  - DevOps
  - PHP
  - Prestashop
  - Reusable code
tags:
  - devops
  - prestashop
---
Vous pouvez accéder à une démo que j&rsquo;ai installé de la dernière version de Prestashop [ici](http://latrmouh.org/prestashop).

# Gestion d&rsquo;environnements

_Références vers la racine de la boutique_

  * **.htaccess** à la racine du projet
  * Tables **ps_configuration** et **ps\_shop\_url**.

_Références vers la base de données_

  * Fichier app/config/parameters.php

<pre class="EnlighterJSRAW" data-enlighter-language="php">&lt;?php return array (
  'parameters' =&gt; 
  array (
    'database_host' =&gt; 'host',
    'database_port' =&gt; '',
    'database_name' =&gt; 'db_name',
    'database_user' =&gt; 'db_user',
    'database_password' =&gt; 'db_pwd',
    'database_prefix' =&gt; 'tbl_prefix',
    'database_engine' =&gt; 'InnoDB',
    'mailer_transport' =&gt; 'smtp',
    'mailer_host' =&gt; '127.0.0.1',
    'mailer_user' =&gt; NULL,
    'mailer_password' =&gt; NULL,
    'secret' =&gt; '75En87VA6bfCemg6GZF7eAFJd2jdK6yFDZ9kGE0BFXuHdAyzID1z7W7d',
    'ps_caching' =&gt; 'CacheMemcache',
    'ps_cache_enable' =&gt; false,
    'ps_creation_date' =&gt; '2016-11-01',
    'locale' =&gt; 'en-US',
    'cookie_key' =&gt; '',
    'cookie_iv' =&gt; '',
    'new_cookie_key' =&gt; 'def00000b022f8a238accf3dbce07c8637935009e0a5ea637e8d1611e06d0ce97edf93af5cf40871d560287eef4990de0801a01df04fbb002184c3e8804d73939d2720e8',
  ),
);</pre>

&nbsp;

# Activation du mode debug

<pre class="EnlighterJSRAW" data-enlighter-language="null">// Dans le fichier config/defines.inc.php
if (!defined('_PS_MODE_DEV_')) {
define('_PS_MODE_DEV_', true);
}
</pre>

&nbsp;

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->