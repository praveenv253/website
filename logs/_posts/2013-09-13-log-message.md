---
layout: blog
title: Timing in C++
date: 2013-09-13 17:04:17 +0530
day: Friday
tags:
  - log message
  - timing
  - profiling
---

Use the `<chrono>` library. `std::chrono::high_resolution_clock` seems to do the trick. It should be giving me nanosecond resolution, but gives me only microsecond resolution. Nevertheless, better than `clock()` any day!