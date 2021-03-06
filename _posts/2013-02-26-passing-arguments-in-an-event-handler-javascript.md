---
id: 34
title: 'Passing arguments in an event handler &#8211; Javascript'
date: 2013-02-26T23:19:15+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=34
permalink: /en/passing-arguments-in-an-event-handler-javascript/
categories:
  - Bugs
  - Javascript
tags:
  - bug
  - javascript
  - leaflet
---
<div class="post-body">
  <p>
    I had this problem while working on Leaflet but I think it can be generalized to the issue of passing parameters to an event handler in Javascript. With the « bind » method of jQuery, you can pass parameters by using the data property of event (the object sent when an event is triggered) :
  </p>
  
  <pre class="EnlighterJSRAW" data-enlighter-language="javascript" data-enlighter-linenumbers="false">
$(marker).bind("click", { parameter : its_value, parameter2: its_value }, function(event) {
console.log("Your parameter is :" + event.data.parameter);
console.log("Your parameter2 is :" + event.data.parameter2);
// your code goes here
});
</pre>
  
  <p>
    As « <em>marker</em> » was a L.Marker object, I had to convert it into a jQuery object before applying the bind method. <a href="http://stackoverflow.com/questions/3994527/passing-parameters-to-click-bind-event-in-jquery" target="_blank">Thank you Anurag on StackOverflow !!</a>
  </p>
</div>

<div class="post-footer">
</div>

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->