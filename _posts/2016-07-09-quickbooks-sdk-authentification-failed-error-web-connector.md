---
id: 330
title: 'Quickbooks SDK &#8211; Authentification failed error (Web connector)'
date: 2016-07-09T12:32:38+00:00
author: leiluspocus
excerpt: How to solve the Authentication Failed error from the webconnector of Quickbooks
layout: post
guid: http://latrmouh.org/blog/?p=330
permalink: /en/quickbooks-sdk-authentification-failed-error-web-connector/
categories:
  - Bugs
  - PHP
tags:
  - quickbooks
---
I used [this SDK](https://github.com/consolibyte/quickbooks-php) to develop an API that connects directly to Quickbooks.

I had this error once: Authentification failed when I tried to fetch data from the API. My identifiers were correct.

The problem came from some warnings I had in my program.

It may sound obvious but make sure you have no PHP errors or warning in your application. Otherwise, the web connector of Quickbooks won&rsquo;t be able to read data from your API.

<u>2017 update</u>
  
Seems like [Quickbooks developed its own SDK.](https://github.com/intuit/QuickBooks-V3-PHP-SDK) It might be a better option to use for your APIs ?

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->