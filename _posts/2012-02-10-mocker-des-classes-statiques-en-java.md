---
id: 5
title: Mocker des classes statiques en Java
date: 2012-02-10T17:43:15+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=5
permalink: /fr/mocker-des-classes-statiques-en-java/
categories:
  - Java
tags:
  - java
  - tdd
---
De nombreux frameworks existent pour la réalisation de tests unitaires en Java, j&rsquo;ai notamment eu l&rsquo;occasion d&rsquo;utiliser JUnit, auquel on peut brancher des librairies facilitant la réalisation de mocks (objects fictifs servant à tester l&rsquo;application).

J&rsquo;ai eu l&rsquo;occasion d&rsquo;utiliser [Mockito](http://mockito.org), assez pratique jusqu&rsquo;au moment où on doit mocker des classes statiques. [PowerMock](https://code.google.com/p/powermock/wiki/MockStatic) répond alors mieux à ce problème.

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->