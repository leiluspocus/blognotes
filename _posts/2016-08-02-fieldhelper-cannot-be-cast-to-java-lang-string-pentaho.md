---
id: 240
title: FieldHelper cannot be cast to java.lang.String pentaho
date: 2016-08-02T13:11:20+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=240
permalink: /en/fieldhelper-cannot-be-cast-to-java-lang-string-pentaho/
categories:
  - Java
  - Pentaho
tags:
  - etl
  - java
  - pentaho
---
I had the following error in a « User Defined Java Class » step on Pentaho Data Integration.

<pre>FieldHelper cannot be cast to java.lang.String</pre>

Indeed, you have to use the getRow() method to convert the field you&rsquo;re getting into a String or any other variable type.

<pre class="EnlighterJSRAW" data-enlighter-language="java">public boolean processRow(StepMetaInterface smi, StepDataInterface sdi) throws KettleException, Exception
{
  Object[] r = getRow();
        if (r == null) { return false; }
        String myString = get(Fields.In, "FeedSubmissionId").getString(r);
}</pre>

&nbsp;

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->