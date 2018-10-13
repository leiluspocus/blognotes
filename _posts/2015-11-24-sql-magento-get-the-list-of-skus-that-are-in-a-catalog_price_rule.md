---
id: 72
title: 'SQL Magento &#8211; Get the list of SKUs that are in a catalog_price_rule'
date: 2015-11-24T12:16:55+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=72
permalink: /en/sql-magento-get-the-list-of-skus-that-are-in-a-catalog_price_rule/
categories:
  - Magento
tags:
  - magento
  - sql
---
The parameter « rule_id » can be viewed in the URL when you are editing the catalog price rule.

<pre class="EnlighterJSRAW" data-enlighter-language="sql" data-enlighter-linenumbers="false">select sku
from catalog_product_entity
where entity_id in (
SELECT DISTINCT product_id 
FROM catalogrule_product 
WHERE rule_id=&lt;rule_id&gt;
);
</pre>

&nbsp;

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->