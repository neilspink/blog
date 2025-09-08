---
title: "AheadFork: Exploring Forks Ahead of Upstream"
date: 2020-11-27
draft: false
---

I wrote **AheadFork**, a small Python tool that helps explore GitHub forks that are ahead of their upstream repository—where contributors have built new code on top of existing projects. Using the GitHub REST API, it checks each fork of a given repo, compares its `master` branch against upstream, and reports how many commits it is ahead or behind, along with stars and last push date. This makes it easy to spot active forks that may contain interesting features, bug fixes, or experiments worth tracking. AheadFork is simple to run with Python 3 and `requests`, and it’s released on GitHub for anyone curious about how projects evolve through their forks.

Check out the [source on GitHub](https://github.com/neilspink/aheadfork) and try it out on your favorite repos.
