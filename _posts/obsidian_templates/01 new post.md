---
layout: post
title:  "<% tp.system.prompt('What is the post title?', '', true, false) %>"
date:   <% tp.date.now() %>
---

<%* 
let permaLink = await tp.system.prompt("Permalink?");
-%> 

<% tp.file.rename(tp.date.now() + "-" + permaLink) %>