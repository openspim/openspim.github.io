---
title: Welcome to µOpenSPIM
layout: page
description: Welcome to µOpenSPIM
---

µOpenSPIM is an intuitive graphical user interface (GUI) for OpenSPIM users, which relies on [µManager](https://micro-manager.org). You can also visit our [Github website](https://github.com/openspim/micro-OpenSPIM).

<table>
<tr class="header">
<th>Acquisition window</th>
<th>Features</th>
<th>Logo</th>
</tr>

<tr class="odd">
<td align="center"><a href="https://openspim.org/images/Figure5_Acquisition-panel_website.png" target="_blank" title="Click for a higher resolution image"><img src="https://openspim.org/images/Figure5_Acquisition-panel_website.png" width="400"></a></td>
<td align="left">
&nbsp;&nbsp;&nbsp;-   A complete overhaul of the GUI&nbsp;&nbsp;&nbsp;</br>
&nbsp;&nbsp;&nbsp;-   An improved control over Picard’s 4D-stage&nbsp;&nbsp;&nbsp;</br>
&nbsp;&nbsp;&nbsp;-   A user-friendly way of setting up multiview time lapse recordings&nbsp;&nbsp;&nbsp;</br>
&nbsp;&nbsp;&nbsp;-   Time-laspe with periodic and sporadic intervals and breaks&nbsp;&nbsp;&nbsp;</br>
&nbsp;&nbsp;&nbsp;-   A quick save function for nearly all acquisitions settings&nbsp;&nbsp;&nbsp;</br>
&nbsp;&nbsp;&nbsp;-   Different saving formats including the n5 format&nbsp;&nbsp;&nbsp;</br>
&nbsp;&nbsp;&nbsp;-   ArduinoUNO support&nbsp;&nbsp;&nbsp;</br>
&nbsp;&nbsp;&nbsp;-   On-the-fly image processing&nbsp;&nbsp;&nbsp;</br>
&nbsp;&nbsp;&nbsp;-   Improved drift-correction functionality&nbsp;&nbsp;&nbsp;</br>
<td align="center"><a href="https://openspim.org/images/%C2%B5OS_Logo.png" target="_blank" title="Click for a higher resolution image"><img src="https://openspim.org/images/%C2%B5OS_Logo.png" width="150"></a>
</td>
</tr>
</table>

## Requirements
-   All hardware components of an OpenSPIM system (Laser, Camera, Stage, etc.) have to be pre-configured with µManager's Hardware Configuration Wizard using Version 2.0 gamma (nightly build 03 May 2021) on a Windows7/10 computer.
-   µOpenSPIM has been tested with Picard's USB 4D-Stage in mind. Using different 4D-Stages should work but could lead to unexpected behaviour.

## How to set up µManager?
-   [Click here](/micro-openspim_micromanager-configuration) if you have never created a working .cfg file with µManager before or/and want to get guidance on configuring multiple cameras, pixel size calibration and configuring an ArduinoUNO board for µManager.

## Installation and start-up
µOpenSPIM is in its beta stage and works with µManager 2.0.0 20210503 for Windows (nightly build 3rd May 2021).</br>
1.  Download and install the [64-bit build of µManager ](https://download.micro-manager.org/nightly/2.0.0-gamma/Windows/MMSetup_64bit_2.0.0-gamma1_20210503.exe) and follow its *Hardware Configuration Wizard* to create a functional configuration file (.cfg) that allows µManager to control the OpenSPIM hardware. On the first time startup of µOpenSPIM users will be asked to select the file location of µManager.

2.	**Download the latest version of µOpenSPIM 1.0.11 (28. November 2024)**
	-	[Win64bit](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.11/OpenSPIM_setup_1.0.11.exe)
	-	[MACOSX](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.11/OpenSPIM-1.0.11.dmg)

3.  In the starting window multiple µManager configuration files can be added, removed and selected. Click *Add .cfg file* to add and then select your working µManager configuration file ending with .cfg. Then click the *Start* button. After loading the hardware µManager should now be ready for use.

<details><summary>Click for µOpenSPIM's changes and previous versions:</summary>
<p>

####	1.0.11 (18. November 2024) [Win64bit](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.11/OpenSPIM_setup_1.0.11.exe), [MACOSX](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.11/OpenSPIM-1.0.11.dmg)
-	Use MMStudio 2.0.0-gamma1-20210503. Please use this version of MIcroManager.
    -	Download [MMSetup_64bit_2.0.0-gamma1_20210503](https://download.micro-manager.org/nightly/2.0.0-gamma/Windows/MMSetup_64bit_2.0.0-gamma1_20210503.exe)
    -	All other updated versions don't seem to work `SnapImage` during acquisition.
-	`showErrorOn = false` during acquisition
-	Fix for unresponsive UI
-	Use `CompletableFuture` for acquisition
-	Include `MMAcqEngine.jar`
-	Security update

####	1.0.10 (19. January 2024) [Win64bit](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.10/OpenSPIM_setup_1.0.10.exe), [MACOSX](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.10/OpenSPIM-1.0.dmg)
-	New filename scheme for acquisition files
-	BigStitcher support
-	Mastodon support

####	1.0.9 (17. August 2022) [Win64bit](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.9/microOpenSPIM_setup_1.0.9.exe), [MACOSX](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.9/microOpenSPIM-1.0.9.dmg)
-	BigDataViewer interface added
-	BigDataViewer compatible N5 storage implemented
-	Fixed non-ascii folder name (hotfix included)

####	1.0.8 (22. July 2022) [Win64bit](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.8/microOpenSPIM_setup_1.0.8.exe), [MACOSX](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.8/microOpenSPIM-1.0.8.dmg)
-	Fixed an issue that opening N5 format corrupts the current dataset

####	1.0.7 (17. June 2022) [Win64bit](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.7/OpenSPIM_setup_1.0.7.exe), [MACOSX](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.7/microOpenSPIM-1.0.7.dmg)
-	Fixed an Anti-Drift bug
-	Fixed that windows has an issue for generating a jar file

####	1.0.6 (12. April 2022) [Win64bit](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.6/microOpenSPIM_setup_1.0.6.exe), [MACOSX](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.6/microOpenSPIM-1.0.6.dmg)
-	Major update in PositionList
-	Improved the logic to handle Z-stack setting
-	"Update position" update the position with the current X, Y, R, Z with Z-Stack setting

####	1.0.5 (22. March. 2022) [Win64bit](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.5/microOpenSPIM_setup_1.0.5.exe), [MACOSX](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.5/microOpenSPIM-1.0.5.dmg)
-	Anti-Drift preprocess: gaussian blur(sigma=2), convolve filter and maximum filter
-	Tickboxes of the positions
-	Fixed wrong percentage indicator
-	Removed the verbose messages
-	Fixed false warning sign that there is the filename already exists
-	Removed null-MPI issue when unchecked MIP option
-	Updated labels for Z-Stacks
-	Added position name and color to distinguish "Stack" and "Position" in the position list
-	Added the name for "Save current position"

####	1.0.4 (15. Nov. 2021) [Win64bit](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.4/OpenSPIM_setup_1.0.4.exe), [MACOSX](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.4/OpenSPIM-1.0.4.dmg)
-	Save/load functions for beanshell and java script
-	Added example fusion scripts
-	Supported ClijX in script panel
-	Updated help files
-	Added the citation information in LoadingDialog window



</p>
</details>

## Contact

Please post feedback, software bugs and questions to the [Image.sc forum](https://forum.image.sc/t/issues-feedback-and-questions-using-openspim/65264).</br>
In case you experienced an issue using µOpenSPIM, it can help to add the related Log file, which is placed in your Micro-Manager folder.
</br>
## Continue to [Image acquisition](/micro-openspim_acquisition)
