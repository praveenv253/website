---
layout: blog
title: const variables in C/C++ and multiple definition errors
date: 2014-02-18 00:44:49 +0530
day: Tuesday
tags:
  - log message
  - C
  - C++
  - headers
  - const
  - static
  - multiple definition error
---

If you have defined a variable in a header file and not declared it as `const`, like so: `double e = 2.71;` then the compiler will treat it as a separate variable in each translation unit. So if you link two such translation units together under the same object later, you will get a multiple definition error, or something like "already defined in...". To solve this issue, mark this variable as `static const` (in C), or as simply `const` (in C++, where static is implied for const variables). What this does is to make the linkage of this variable definition _internal_, meaning that once this definition gets `#include`d into a .c or .cpp file, the definition stays there. It does not have scope outside of the translation unit, and thus cannot be seen by the other object files. On the other hand, the addresses of each of these "copies" of the constant in different translation units will be different. To have a "true" global constant this way, you will need to have an `extern const double e;` in your header file, followed by a `const double e = 2.71;` in a separate source file, which is compiled into a separate object file, _which_ then gets linked with all the other objects. Courtesy of [this SO post](http://stackoverflow.com/questions/2328671/constant-variables-not-working-in-header).