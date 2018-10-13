---
id: 155
title: How to add a new stock option in Woocommerce
date: 2016-03-22T18:53:53+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=155
permalink: /en/how-to-add-a-new-stock-option-in-woocommerce/
categories:
  - PHP
  - Reusable code
  - Woocommerce
tags:
  - javascript
  - jquery
  - php
---
Sometimes, clients can come up with some pretty creative ways to handle their inventory &#8230; It was the case for me with a customer who was using WooCommerce.

I had to add a third option but the stock options was not customizable. I ended up deleting the native dropdown of stock options and I implemented a custom field.

In functions.php

<pre class="EnlighterJSRAW" data-enlighter-language="php">add_action('woocommerce_product_options_stock_status', 'add_custom_stock_type');    
function add_custom_stock_type() {
        // Stock status - We remove the default one
        ?&gt;
        &lt;script type="text/javascript"&gt;
            jQuery('_stock_status').remove();
        &lt;/script&gt;
        &lt;?php   
    }</pre>

And then I followed [this tutorial](http://www.remicorson.com/mastering-woocommerce-products-custom-fields/) to create a custom field : http://www.remicorson.com/mastering-woocommerce-products-custom-fields/

[Someone on SO](http://stackoverflow.com/questions/26912556/add-stock-option-in-woocommerce/26916930#26916930) proposed an other solution based on my approach but my contract was already done with that client by the time he answered, didn&rsquo;t get the chance to test it out.

&nbsp;

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->