---
id: 42
title: 'Parsing errors &#8211; JSON'
date: 2013-06-25T23:26:03+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=42
permalink: /en/parsing-errors-json/
categories:
  - Bugs
  - Javascript
tags:
  - javascript
  - json
---
<div class="post-body">
  <p>
    Parsing JSON with the jQuery method $.parseJSON can be tricky to debug, specially when you&rsquo;re using a mobile device. Here are a list of errors I encoutered, and the reason why they were raised.
  </p>
  
  <p>
    <b>Unexpected token u </b><br /> The method tries to parse a undefined variable.
  </p>
  
  <p>
    <b>Unexpected token o </b><br /> The method tries to parse [Object object].
  </p>
</div>

<div class="post-footer">
</div>

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->