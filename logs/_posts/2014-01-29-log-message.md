---
layout: blog
title: xsessionrc and xmodmap
date: 2014-01-29 18:55:44 +0530
day: Wednesday
tags:
  - log message
  - xinitrc
  - X
  - xsessionrc
---

In order to have your `xmodmap` commands take effect, put them in `.xsessionrc`, NOT `.xinitrc`. Take a look at [this](http://askubuntu.com/questions/150487/what-happens-under-the-covers-to-log-me-in-and-start-up-the-unity-graphics-user). Also, `man xmodmap` for a few examples of remapping keys.