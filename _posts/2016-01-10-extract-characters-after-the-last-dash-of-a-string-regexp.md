---
id: 109
title: 'Extract characters after the last dash of a String &#8211; RegExp'
date: 2016-01-10T16:51:21+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=109
permalink: /en/extract-characters-after-the-last-dash-of-a-string-regexp/
categories:
  - PHP
  - Reusable code
tags:
  - php
  - regexp
---
I wanted to extract characters after the last dash of a string. Regular expression are such a powerful tool to use in these cases. Here&rsquo;s the one I needed for my problem :

<pre class="EnlighterJSRAW" data-enlighter-language="null">(\w+)[^-]*$</pre>

Please note that with PHP, you need to use the preg_match method and surround the regexp with slashes.

<pre class="EnlighterJSRAW" data-enlighter-language="php">preg_match ('/(\w+)[^-]*$/', 'cgo3020-red-xs', $results); // returns xs in $results[0]</pre>

Here&rsquo;s a pretty convenient tool to test your regexp:  https://regex101.com/

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->