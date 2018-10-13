---
id: 107
title: 'PHP / Magento &#8211; Direct SQL Queries'
date: 2015-12-22T11:37:54+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=107
permalink: /en/php-magento-direct-sql-queries/
categories:
  - Magento
  - PHP
tags:
  - magento
  - php
---
Not the cleanest but here&rsquo;s a quick solution to do a direct query on Magento. Might be faster than calling Magento&rsquo;s objects ? 

<pre class="EnlighterJSRAW" data-enlighter-language="php">/**
   * Get the resource model
   */
$resource = Mage::getSingleton('core/resource');
     
 /**
  * Acccess to the database in read only
  */
$readConnection = $resource-&gt;getConnection('core_read');
     
$query = 'SELECT * FROM ' . $resource-&gt;getTableName('catalog/product');
     
/**
 * Execute the query  
 */
$results = $readConnection-&gt;fetchAll($query);
</pre>

[Thank you DevProblems !](http://www.devproblems.com/magento-direct-sql-queries/)

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->