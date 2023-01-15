---
title: Guide to Monorepos for Front-End Code
author: Alexander Noel
cover: https://bs-uploads.toptal.io/blackfish-uploads/components/seo/content/og_image_file/og_image/777662/guide-to-monorepos-fa73089d7b8fb09108d6433140e040ab.png
dateRead: 
status: 
tag: 
type:articles
---
![rw-book-cover](https://bs-uploads.toptal.io/blackfish-uploads/components/seo/content/og_image_file/og_image/777662/guide-to-monorepos-fa73089d7b8fb09108d6433140e040ab.png)

## Metadata
- Author: [[Alexander Noel]]
- Full Title: Guide to Monorepos for Front-End Code
- Category: #articles
- URL: https://www.toptal.com/front-end/guide-to-monorepos

## Highlights
- A monorepository is a code management and architectural concept whereby you keep all your isolated bits of code in one super repository instead of managing multiple smaller repositories—like a single repository for your website and mobile apps. ([View Highlight](https://read.readwise.io/read/01gpe60e70eze42cs6x0g2knx8))
- If you are thinking about architecture, you will want to do two main things: Separate concerns and avoid code dupes ([View Highlight](https://read.readwise.io/read/01gpg52rt9a5wk6nr6n00vzwfd))
- Instead of having a lot of repositories with their own configs, we will have only one source of truth—the monorepo: one test suite runner, one Docker configuration file, and one configuration for Webpack. ([View Highlight](https://read.readwise.io/read/01gpg69bxqq99paqg70jyzhph4))
- Since everything is located inside one repo, you can configure your CI/CD and bundler once and then just re-use configs to build all packages before publishing them to remote. Same goes for unit, e2e, and integration tests—your CI will be able to launch all tests without having to deal with additional configuration. ([View Highlight](https://read.readwise.io/read/01gpg6b1n08dyg5t39hp4rqtxf))
- No need to re-install dependencies in each repo whenever you want to update your dependencies ([View Highlight](https://read.readwise.io/read/01gpg6en0ycx2kxwnhdgtgvsqa))
- You can use a reference to the remote package and consume them via a single entry point. To use the local version, you are able to use local symlinks. This feature can be implemented via bash scripts or by introducing some additional tools like Lerna or Yarn. ([View Highlight](https://read.readwise.io/read/01gpg6fp5h5g8gjvgpw3kqhb02))
- you can’t share only the part of your monorepo—you will have to give access to the whole codebase, which might lead to some security issues. ([View Highlight](https://read.readwise.io/read/01gpg6ggpyvskvm36txrgzjhyw))
- Bazel is a build tool for large-scale applications, which can handle multi-language dependencies and support a lot of modern languages (Java, JS, Go, C++, etc. ([View Highlight](https://read.readwise.io/read/01gpg6kv7gvtxcq8em8f1xxdwk))
- Loosely coupled code has proven to be more reliable because it allows us to introduce changes without being afraid to break things in other places ([View Highlight](https://read.readwise.io/read/01gpg6p0d20411j9hkccvw6022))
