---
layout: blog
title: cset for partitioning user and system processes
date: 2013-09-14 15:44:13 +0530
day: Saturday
tags:
  - log message
  - timing
  - profiling
  - taskset
  - cpuset
  - cset
---

`taskset` only allows you to set something called the CPU affinity, meaning you can tell the system to run a certain process on some cores only. However, in order to tell the OS to run only your process on a given core, you need to use something called `cpuset`. This is a pseudo-filesystem which manages how processes are distributed among cores. `man cpuset` for more info. While `cpuset` is nice and everything, it is not very intuitive to use, especially if you just want to run your own process(es) separately from the general bunch of system-upkeep processes. A nice interface for cpuset is `cset`, whose `shield` command does exactly this. `man cset` and `cset-shield` for more info. Also take a look at [this tutorial](https://www.suse.com/documentation/slerte_11/slerte_tutorial/data/slerte_tutorial.html). If you are hell bent on using `cpuset` nonetheless, just remember that moving `sbin/init` into the system cpuset along with the "general" lot of processes ensures that any newly spawned processes are also restricted to _that_ cpuset. Oh and dont forget to set the `cpu_exclusive` flag.