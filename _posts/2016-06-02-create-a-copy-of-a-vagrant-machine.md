---
id: 209
title: Create a copy of a Vagrant machine
date: 2016-06-02T18:09:22+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=209
permalink: /en/create-a-copy-of-a-vagrant-machine/
categories:
  - DevOps
tags:
  - vagrant
---
1. Stop your vagrant machine

<pre class="EnlighterJSRAW" data-enlighter-language="shell">vagrant halt</pre>

2. Create the copy (it can take sometime)

<pre class="EnlighterJSRAW" data-enlighter-language="shell">vagrant package --base &lt;name_of_your_machine&gt;  --output path/to/newly/created/package</pre>

The machine name is on Virtual Box 🙂

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->