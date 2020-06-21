---
layout: blog
title: Vim modelines
date: 2013-09-15 17:33:16 +0530
day: Sunday
tags:
  - log message
  - vim
  - filetype
---

If vim does not detect a filetype correctly, then you can add a modeline at the top of the file (first or second line, I think), which tells vim the filetype. For example, when the tex class file mycv.cls was incorrectly detected (as a Java class file, I presume), I added the modeline `% vim: set filetype=tex :` right at the top. This resolved the problem. Do a `:help filetype` for more info. 