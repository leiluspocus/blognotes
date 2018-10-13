---
id: 212
title: Write a new task using Capistrano
date: 2016-07-18T16:31:43+00:00
author: leiluspocus
layout: post
guid: http://latrmouh.org/blog/?p=212
permalink: /en/create-a-new-task-capistrano/
categories:
  - DevOps
tags:
  - capistrano
---
Capistrano can be a great tool to run a task on several servers. It can be a task like uploading a maintenance page or deleting some logs :

<pre class="EnlighterJSRAW" data-enlighter-language="null">task :NAME_OF_YOUR_TASK do
desc &lt;&lt;-DESC
This is my awesome task. Description appears in help so write it carefully.
DESC
run "rm -rf #{logs_folder}"
run "mkdir #{destination_folder}"
top.upload("index.html", "#{destination_folder}/index.html")
end</pre>

You can read more about writing Capistrano tasks [here](http://vladigleba.com/blog/2014/04/10/deploying-rails-apps-part-6-writing-capistrano-tasks/).

&nbsp;

<!-- AddThis Advanced Settings generic via filter on the_content -->

<!-- AddThis Share Buttons generic via filter on the_content -->