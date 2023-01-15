---
title: You Want Modules, Not Microservices
author: Ted Neward
cover: https://readwise-assets.s3.amazonaws.com/static/images/article4.6bc1851654a0.png
dateRead: 
status: 
tag: 
type:articles
---
![rw-book-cover](https://readwise-assets.s3.amazonaws.com/static/images/article4.6bc1851654a0.png)

## Metadata
- Author: [[Ted Neward]]
- Full Title: You Want Modules, Not Microservices
- Category: #articles
- URL: https://blogs.newardassociates.com/blog/2023/you-want-modules-not-microservices.html

## Highlights
- Unlike traditional service-oriented architectures (SOAs), which typically involve heavyweight inter-process communications protocols, microservices use event-streaming technologies to enable easier integration ([View Highlight](https://read.readwise.io/read/01gnwndyj7y1sgh0wepgpba1zv))
- [Pipes-and-filters](http://blogs.newardassociates.com/patterns/behavioral/PipesAndFilters) architectures have been a part of the software scene since the 70s, when [Unixes promoted several ideas](https://en.wikipedia.org/wiki/Unix_philosophy):
  1. Make each program do one thing well. To do a new job, build afresh rather than complicate old programs by adding new "features".
  2. Expect the output of every program to become the input to another, as yet unknown, program. Don't clutter output with extraneous information. Avoid stringently columnar or binary input formats. Don't insist on interactive input ([View Highlight](https://read.readwise.io/read/01gnwnfvd86393w447fve6dx5c))
- at a conceptual level, they're all modules. Each has a different internal format, but each serves the same basic purpose: an independently-built, -managed, -versioned, and -deployed unit of code that can be reused ([View Highlight](https://read.readwise.io/read/01gnz3a6erxsxbrb4q3v6b4b9t))
- it meant that each team could build their artifact independently of one another, constrained by nothing other than time and the physics of how fast fingers can fly over a keyboard.
  In theory, anyway. ([View Highlight](https://read.readwise.io/read/01gnz3ff3g84whaxt9ma5jb9nc))
- When passing that data across network lines, though--as most microservices do--adds five to seven orders of magnitude greater latency to the communication. That is not simply something we can "scale away" by adding more nodes to the network; that actually makes the problem worse. ([View Highlight](https://read.readwise.io/read/01gnz3hc7w5p6yshrb3v5rdm3h))
- The key is to establish that common architectural backplane with well-understood integration and communication conventions, whatever you want or need it to be. ([View Highlight](https://read.readwise.io/read/01gnz3k98jpaqj4wdxb4yz2b7f))
- ***Do you need to reduce the dependencies your development team is facing?*** Then begin by looking at those dependencies and working with partners to determine which of them you can bring into the team's wheelhouse ([View Highlight](https://read.readwise.io/read/01gnz3m9s1xjyzv756kkftc3xp))
- But, most importantly, make sure that team has a crystal-clear vision of what it is they're trying to build, and they can confidently describe the heart of their service/microservice/module to any random stranger walking by on the street. ***The key is to give the team the direction and goal, the autonomy to accomplish it, and the clarion call to get it done.*** ([View Highlight](https://read.readwise.io/read/01gnz3mv84fe60w5aph3vnnp39))
