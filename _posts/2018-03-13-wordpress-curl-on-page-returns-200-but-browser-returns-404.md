---
id: 388
title: 'WordPress &#8211; Curl on page returns 200 but browser returns 404'
date: 2018-03-13T17:37:20+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=388
permalink: /en/wordpress-curl-on-page-returns-200-but-browser-returns-404/
categories:
  - Bugs
  - PHP
tags:
  - bugs
  - http status code
  - php
---
I had a weird issue on a PHP script. I was returning an error 404 on a WordPress page the following way :

<pre class="EnlighterJSRAW" data-enlighter-language="null">// At the beginning of a template page
global $wp_query;

  if ( $posts_query-&gt;post_count == 0 ) {
    $wp_query-&gt;set_404();
    status_header(404);
    get_template_part( 404 ); die();
  }</pre>

When I was accessing the error page on the browser, It worked well, I had a 404 error page displayed + the correct status code when I inspected the page (Network tab).

However, when I was « curl-ing » the same error page, it didn&rsquo;t work. It didn&rsquo;t work in the shell, or in the PHP script.

The Shell command I did :

<pre class="EnlighterJSRAW" data-enlighter-language="null">$ curl -I http://myerrorpage.dev 
HTTP/1.1 200 OK
Date: Tue, 13 Mar 2018 16:24:08 GMT
Server: Apache/2.4.7 (Ubuntu)
X-Powered-By: PHP/5.5.9-1ubuntu4.22
Expires: Thu, 19 Nov 2018 08:52:00 GMT
Cache-control: max-age=0, no-store
Set-Cookie: wordpress_fd4fa864532af79923254c1877e41f25=+; expires=Mon, 13-Mar-2017 16:24:09 GMT; Max-Age=-31536000;</pre>

The buggy PHP Script

<pre class="EnlighterJSRAW" data-enlighter-language="null">$ch = curl_init();
curl_setopt($ch, CURLOPT_URL,            $url);
curl_setopt($ch, CURLOPT_HEADER,         true);
curl_setopt($ch, CURLOPT_NOBODY,         true);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_TIMEOUT,        1);
$headers[] = curl_exec($ch);
$status = curl_getinfo($ch, CURLINFO_HTTP_CODE);
var_dump($status);</pre>

## 

## Solution

I had to remove the « CURLOPT_NOBODY » to get the correct status code.

<pre class="EnlighterJSRAW" data-enlighter-language="null">$ch = curl_init();
curl_setopt($ch, CURLOPT_URL,            $url);
curl_setopt($ch, CURLOPT_HEADER,         true);
// curl_setopt($ch, CURLOPT_NOBODY,         true);
curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);
curl_setopt($ch, CURLOPT_TIMEOUT,        1);
$headers[] = curl_exec($ch);
$status = curl_getinfo($ch, CURLINFO_HTTP_CODE);
var_dump($status);</pre>

&nbsp;

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->