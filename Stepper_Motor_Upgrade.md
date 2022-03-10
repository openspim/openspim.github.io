---
title: Stepper Motor Upgrade
layout: page
description: Additional setup tweaks
---

Instructions about how to go about this for a Thorlabs DRV001 connected via a Thorlabs BSC201 controller on a 64bit OpenSPIM setup are detailed below (by Jerome Boulanger and Ben Sutcliffe):

1.  Download the micro-manager source code as instructed [here](https://micro-manager.org/wiki/Micro-Manager_Source_Code).
2.  Install all the relevant programs for building micro-manager as instructed [here](https://micro-manager.org/wiki/Building_MM_on_Windows).
3.  Setup up Visual C++ 2010 Express as [here](https://micro-manager.org/wiki/Visual_Studio_project_settings_for_device_adapters).
4.  Install the 64bit APT software from [Thorlabs](https://www.thorlabs.com/software_pages/ViewSoftwarePage.cfm?Code=Motion_Control&viewtab=1).
5.  Download and unzip the APTx64 form [here](https://micro-manager.org/wiki/File:APT_x64.zip).
6.  Then build the ThorlabsAPTStage Device Adapter in 64bit on a 64bit Windows 7 machine, using the 'APT.lib' downloaded in point 5.
7.  Rename the resulting .dll file to 'mmgr_dal_ThorlabAPTStage.dll' then place it into the OpenSPIM.app folder along with the 'APT.dll' downloaded in 5).
8.  The OpenSPIM Fiji/MM bundle can then restarted and a ThorlabAPTStage could be configured as described for a 32bit system [here](https://micro-manager.org/wiki/ThorlabsAPTStage).