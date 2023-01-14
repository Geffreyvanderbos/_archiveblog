---
layout: post
title:  "<%* let postTitle = await tp.system.prompt("What is the post title?");-%><% postTitle %>"
date:   <% tp.date.now("YYYY-MM-DD HH:MM:SS Z") %>
---

<%* 
function makePermalink(string){
	var lis = string.split(" ")
	string = lis.join("-");
	return string;
}

let permaLink = makePermalink(postTitle).toLowerCase();
-%> 

<% tp.file.cursor() %>

<% tp.file.rename(tp.date.now() + "-" + permaLink) %> 