---
id: 105
title: 'SQL Magento &#8211; Get store credit balance'
date: 2015-12-21T17:48:06+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=105
permalink: /en/sql-magento-get-store-credit-balance/
categories:
  - Magento
tags:
  - magento
  - sql
---
Valid for Magento EE only. The feature of store credits isn&rsquo;t native in CE edition.

<pre class="EnlighterJSRAW" data-enlighter-language="sql">select amount 
from enterprise_customerbalance 
where customer_id = @customer_id ;</pre>

&nbsp;

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->