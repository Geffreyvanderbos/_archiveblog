---
date: 2023-01-15
layout: post
title: "Obsidian as a CMS to publish on Github Pages with Jekyll"
---

I couldn't stop thinking about using Obsidian.md as a content management system for my website.

My previous website used [Grav CMS](https://getgrav.org/) to serve Markdown files. It is great. But, not great for working on in Obsidian because of their odd "folder" based pages.

So, I set-out to rebuild my site on Jekyll. Knowing that I can have a list of Markdown files as posts.

Now, I …

1. installed Jekyll on my computer,
2. opened the `\_POSTS` folder as a Vault in Obsidian.
3. Use Templater to give me a ready to write Markdown file.
4. Use the Obsidian Git plugin to publish the notes to Github Pages.

It works really well.

Below the template I use for posts. On creating a new note, it asks for the post title. It then renames the file with a Jekyll ready permalink.

```
---
layout: post
title:  "<%* let postTitle = await tp.system.prompt("What is the post title?");-%><% postTitle %>"
date:   <% tp.date.now("YYYY-MM-DD") %>
---

<%* 
function makePermaLink(string) {
	var common = getStopWords();
	var wordArr = string.match(/\w+/g),
		commonObj = {},
		uncommonArr = [],
		word, i;

	for (i = 0; i < common.length; i++) {
		commonObj[ common[i].trim() ] = true;
	}

	for (i = 0; i < wordArr.length; i++) {
		word = wordArr[i].trim().toLowerCase();
		if (!commonObj[word]) {
			uncommonArr.push(word);
		}
	}
	return uncommonArr.join("-");
}

let permaLink = makePermaLink(postTitle);

function getStopWords() {
	return ["a", "able", "about", "across", "after", "all", "almost", "also", "am", "among", "an", "and", "any", "are", "as", "at", "be", "because", "been", "but", "by", "can", "cannot", "could", "did", "do", "does", "either", "else", "ever", "every", "for", "from", "get", "got", "had", "has", "have", "he", "her", "hers", "him", "his", "how", "however", "i", "if", "in", "into", "is", "it", "its", "just", "least", "let", "like", "likely", "may", "me", "might", "most", "must", "my", "neither", "no", "nor", "not", "of", "off", "often", "on", "only", "or", "other", "our", "own", "rather", "said", "say", "says", "she", "should", "since", "so", "some", "than", "that", "the", "their", "them", "then", "there", "these", "they", "this", "tis", "to", "too", "twas", "us", "wants", "was", "we", "were", "what", "when", "where", "which", "while", "who", "whom", "why", "will", "with", "would", "yet", "you", "your", "ain't", "aren't", "can't", "could've", "couldn't", "didn't", "doesn't", "don't", "hasn't", "he'd", "he'll", "he's", "how'd", "how'll", "how's", "i'd", "i'll", "i'm", "i've", "isn't", "it's", "might've", "mightn't", "must've", "mustn't", "shan't", "she'd", "she'll", "she's", "should've", "shouldn't", "that'll", "that's", "there's", "they'd", "they'll", "they're", "they've", "wasn't", "we'd", "we'll", "we're", "weren't", "what'd", "what's", "when'd", "when'll", "when's", "where'd", "where'll", "where's", "who'd", "who'll", "who's", "why'd", "why'll", "why's", "won't", "would've", "wouldn't", "you'd", "you'll", "you're", "you've"];
}
-%> 
<% tp.file.cursor(1) %>

<% tp.file.rename(tp.date.now() + "-" + permaLink) %>
```
