---
title: Debugging
layout: page
description: Debuggind software 
---
## Dependency problems (AKA "Module could not be loaded")

If a module cannot be loaded, most likely you are missing one or more .dll files. The easiest way to find out which is to download the [Dependency Walker](https://www.dependencywalker.com/) and open the *dist/mm/win32/mmgr_dal_*.dll* dfile in question.

## The CoreLog

Micro-Manager writes verbose information to the *CoreLog<timestamp>.txt* file in the directory where Fiji was started. This is better in many respects than calling Fiji with the --console option because the latter often has problems when both native and Java code write to the console -- in which case you can see interleaved characters and not make any sense of it at all.

Likewise, it is advisable to use the *ReportingUtils.log()* and *ReportingUtils.logException()* methods to write to the CoreLog from Java.
