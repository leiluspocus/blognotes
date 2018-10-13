---
id: 67
title: VirtualBox CheatSheet
date: 2016-02-18T16:08:10+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=67
permalink: /en/virtualbox-cheatsheet/
categories:
  - DevOps
---
Here is a couple of commands I&rsquo;ve used in a previous life while trying to resize a Vagrant machine.

#### List the virtual disk images used by Virtual Box

<pre class="EnlighterJSRAW" data-enlighter-language="shell">vboxmanage list hdds</pre>

#### Remove a hard disk from a Virtual Box registry

<pre class="EnlighterJSRAW" data-enlighter-language="shell">vboxmanage closemedium disk a5bad1ba-5ff7-4b83-87ff-adb18f05269a --delete 
</pre>

#### [How to resize a hard disk for a Virtual Machine &#8211; Tutorial](https://gist.github.com/christopher-hopper/9755310)

&nbsp;

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->