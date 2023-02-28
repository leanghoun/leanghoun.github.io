---
layout: default
title: Github Pages & Jekyll
parent: Coding
grand_parent: Collections
permalink: /docs/collections/coding/github-pages-jekyll/
nav_order: 1
---

# Github Pages & Jekyll
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

- TOC
{:toc}

---

## References
* [Github Pages](https://docs.github.com/en/pages)
* [Jekyll](https://jekyllrb.com/)
  - [Documentation](https://jekyllrb.com/docs/)
* [Just the Docs Theme](https://github.com/just-the-docs/just-the-docs)
  - [Documentation](https://just-the-docs.github.io/just-the-docs/)


## Installing Dependencies
Jekyll has a few requirements before we can serve up local pages for testing:
* Ruby version 2.5.0 or higher, including all development headers (check your Ruby version using `ruby -v`)
* RubyGems (check your Gems version using `gem -v`)
* GCC and Make (check versions using `gcc -v`,`g++ -v`, and `make -v`)

[Here are step-by-step instructions](https://jekyllrb.com/docs/installation/macos) to get it working on MacOS.

## Testing Locally
To start Jekyll, open a Terminal window:
```
cd Documents/GitHub/leanghoun.github.io/
bundle exec jekyll serve --livereload
```
To reach the local page: [localhost:4000](http://localhost:4000).

## GitHub Pages

This entire website is built on and hosted by [Github Pages](https://docs.github.com/en/pages) with a remote theme called [Just the Docs](https://github.com/just-the-docs/just-the-docs), just like the [Voron Docs](https://docs.vorondesign.com/). The local files are edited with [Nova]({{ site.baseurl }}{% link docs/collections/coding/nova.md %}) and synced back to GitHub via Nova's built-in GitHub integration.