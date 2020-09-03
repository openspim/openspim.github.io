---
title: 64bit OpenSPIM
layout: page
description: 64-bit software information
---
As of April 27th, there is an official (but untested) 64-bit version of the OpenSPIM package [available for download](https://downloads.imagej.net/openspim").

## Use with Andor sCMOS (Neo and Zyla)

For using Andor's sCMOS cameras, take the following steps:

  - install Andor's Driver Pack (get it [here](https://www.andor.com/downloads?src=micro) to the directory where you put mFiji)
  - disable C-states in BIOS
  - in *Control Center > Power Options > PCI express* disable link state power management
  - reboot your computer and turn the camera on and off again

(adapted from <https://micro-manager.org/wiki/Andor_SDK3>)
