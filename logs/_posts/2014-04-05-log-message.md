---
layout: blog
title: IPython-like completion in bash
date: 2014-04-05 11:59:57 +0530
day: Saturday
tags:
  - log message
  - bash
  - command history
  - completion
---

To get ipython-like command completion in bash, i.e. to make it so that bash will only search the subset of history that starts with letters you have already entered so far (thus making it easier to search through history, without having to use the unwieldy Ctrl-R), you need to add a few lines to `.inputrc`. Take a look at [this AU question](http://askubuntu.com/questions/12368/ipython-like-command-history-for-shell for more).