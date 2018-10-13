---
id: 237
title: 'Get XML Data won&rsquo;t parse XML object &#8211; Pentaho'
date: 2016-08-01T17:20:40+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=237
permalink: /en/get-xml-data-wont-parse-xml-object-pentaho/
categories:
  - Pentaho
tags:
  - etl
  - pentaho
---
I had an issue with Pentaho today. It wasn&rsquo;t able to simply parse this XML that I was fetching from Amazon Marketplace Webservice.

Here&rsquo;s the data I got :

<pre class="EnlighterJSRAW" data-enlighter-language="null">&lt;SubmitFeedResponse xmlns="http://mws.amazonaws.com/doc/2009-01-01/"&gt;
&lt;SubmitFeedResult&gt;
&lt;FeedSubmissionInfo&gt;
&lt;FeedSubmissionId&gt;MY_FEED_ID&lt;/FeedSubmissionId&gt;
&lt;FeedType&gt;_POST_INVENTORY_AVAILABILITY_DATA_&lt;/FeedType&gt;
&lt;SubmittedDate&gt;2016-08-01T19:28:30+00:00&lt;/SubmittedDate&gt;
&lt;FeedProcessingStatus&gt;_SUBMITTED_&lt;/FeedProcessingStatus&gt;
&lt;/FeedSubmissionInfo&gt;
&lt;/SubmitFeedResult&gt;
&lt;ResponseMetadata&gt;
&lt;RequestId&gt;MY_REQUEST_ID&lt;/RequestId&gt;
&lt;/ResponseMetadata&gt;
&lt;/SubmitFeedResponse&gt;</pre>

The step « Get XML Data » couldn&rsquo;t parse it because of the xmlns attribute tag. So I had to add a step « Replace in string » that would delete this attribute.

[<img class="alignnone size-thumbnail wp-image-238" src="http://latrmouh.org/blog/wp-content/uploads/2016/08/Screenshot-from-2016-08-01-171856-150x150.png" alt="Screenshot from 2016-08-01 17:18:56" width="150" height="150" />](http://latrmouh.org/blog/wp-content/uploads/2016/08/Screenshot-from-2016-08-01-171856.png)

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->