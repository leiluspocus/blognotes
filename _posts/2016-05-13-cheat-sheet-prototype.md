---
id: 193
title: 'Prototype &#8211; Cheat Sheet'
date: 2016-05-13T20:37:49+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=193
permalink: /en/cheat-sheet-prototype/
categories:
  - Javascript
  - Magento
tags:
  - cheat sheet
  - javascript
  - prototype
---
I had to deal with Prototype while working with Magento. Here&rsquo;s a little cheat sheet of some very simple stuff I had to do.

## Make an Ajax Request with parameters

<pre class="EnlighterJSRAW" data-enlighter-language="js">new Ajax.Request(url, {
                   method:'get',
                   params : { data1 : 'myParam' }
                   onSuccess: function(xhr){
                    console.log(xhr.responseText); 
                    var json = JSON.parse(transport.responseText);
                    }
});</pre>

## Change value of an input

<pre class="EnlighterJSRAW" data-enlighter-language="js">$('ID OF THE ELEMENT').setValue('The new value');</pre>

## Change data within a span tag

<pre class="EnlighterJSRAW" data-enlighter-language="js">$('ID OF THE ELEMENT').update('Your new data');</pre>

&nbsp;

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->