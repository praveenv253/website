---
layout: blog
title: Nautilus&#58; stop showing hidden files when opened from terminal
date: 2015-03-03 20:57:30 -0500
day: Tuesday
tags:
  - log message
  - nautilus
  - hidden files
  - default
---

Nautilus shows hidden files by default when opened from command line. To fix this, go to dconf-editor, and under `org->gtk->settings->file-chooser`, uncheck `show-hidden`. [Link](http://ubuntuforums.org/showthread.php?t=2133298&s=cc010bab19c680d2f485dd0eb8575a28&p=12623240#post12623240).