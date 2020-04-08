---
layout: blog
title: Vim search register
date: 2014-01-09 23:10:39 +0530
day: Thursday
tags:
  - log message
  - vim
  - substitution
  - search
  - registers
---

You can substitute the last search pattern in vim either by omitting the search pattern in the `:%s` command, or by inserting the contents of the search register onto the command line using `<C-r>/`. `<C-r><reg>` can be used anywhere to insert the contents of any register `<reg>`. In this case, the `/` register contains the last search pattern.