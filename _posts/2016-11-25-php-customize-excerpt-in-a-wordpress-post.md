---
id: 265
title: 'PHP &#8211; Customize excerpt in a WordPress post'
date: 2016-11-25T09:05:28+00:00
author: leiluspocus
excerpt: Petit code snippet pour modifier les extraits Wordpress.
layout: post
guid: http://latrmouh.org/blog/?p=265
permalink: /en/php-customize-excerpt-in-a-wordpress-post/
categories:
  - PHP
  - Reusable code
tags:
  - php
  - wordpress
---
<pre class="EnlighterJSRAW" data-enlighter-language="php">add_filter( 'get_the_excerpt', 'my_new_excerpt' );
function my_new_excerpt( $format )
{
    $format = __( ' Blabla' ); // Modify this to your needs!
    return $format;
}
</pre>

&nbsp;

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->