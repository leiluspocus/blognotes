---
id: 40
title: 'Sessions keep refreshing &#8211; CodeIgniter'
date: 2013-06-05T23:22:47+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=40
permalink: /en/sessions-keep-refreshing-codeigniter/
categories:
  - Bugs
  - PHP
tags:
  - bug
  - codeigniter
  - sessions
---
I had a bug once, the sessions kept expiring even though the token was still valid.

I found out that CI\_sessions were refreshing the session\_id all the time. This was a database issue, be careful on the length of the columns in the database. The column that stored the session_id was too short and the token kept being re-generated since the old one couldn&rsquo;t be recognized.

This was a tricky bug because it didn&rsquo;t raise any obvious PHP error&#8230; Be careful with the schema of your database folks !

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->