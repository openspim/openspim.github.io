<img src="https://openspim.org/images/%C2%B5OS_Logo.png" width="200"></a> </br>Welcome! µOpenSPIM is an intuitive new graphical user interface (GUI) for OpenSPIM users, which relies on [µManager](https://micro-manager.org). You can also visit our [Github website](https://github.com/openspim/micro-OpenSPIM).

## Quick Menu
[Image acquisition](/micro-openspim_acquisition)</br>
[Detailed Acquisition controls](/micro-openspim_acquisition-controls)

## Features of µOpenSPIM
<details>
<p>

-   A complete overhaul of the GUI has been made including simple graphic visualizations and an improved control over Picrard’s 4D-stage
-   A user-friendly way of setting up multiview time lapse recordings with several positions and the option to acquire periodic and sporadic intervals with optional breaks during time-lapse recordings
-   A quick save function for nearly all acquisitions settings to save time in case an imaging session is interrupted or a similar session will take place at another time
-   Different saving formats (single plane tiff files, whole stacks or n5 format)
-   ArduinoUNO support
-   On-the-fly image processing
-   new drift-correction functionality
</p>
</details>

## µOpenSPIM requirements
-   All hardware components of an OpenSPIM system (Laser, Camera, Stage, etc.) have to be pre-configured with µManager's Hardware Configuration Wizard using Version 2.0 gamma (nightly build 04 May 2021) on a Windows7/10 computer.
-   µOpenSPIM has been tested with Picard's USB 4D-Stage in mind. Using different 4D-Stages should work but could lead to unexpected behaviour.

## How to set up µManager before using µOpenSPIM?
-   Click [here](/micro-openspim_micromanager-configuration) if you have never created a working .cfg file with µManager before or/and want to get guidance on configuring multiple cameras, pixel size calibration and configuring an ArduinoUNO board for µManager.

## Installation and start-up of µOpenSPIM
-   µOpenSPIM is in its beta stage and works with µManager 2.0.1 20210721 for Windows (nightly build 21 July 2021).
-   Visit our [µOpenSPIM-Github Site](https://github.com/openspim/micro-OpenSPIM) for previous releases and more information.
1.  Please [download](https://valelab4.ucsf.edu/~MM/builds/2.0/Mac/Micro-Manager-2.0.0.dmg) and install the [64-bit](https://valelab4.ucsf.edu/~MM/nightlyBuilds/2.0/Windows/MMSetup_64bit_2.0.1_20210721.exe) build of [µManager](https://micro-manager.org/) and follow its *Hardware Configuration Wizard* to create a functional configuration file (.cfg) that allows µManager to control the OpenSPIM hardware. On the first time startup of µOpenSPIM users will be asked to select the file location of µManager.

2.	**Download µOpenSPIM**
-	[Win64bit](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.4/OpenSPIM_setup_1.0.4.exe)
-	[MACOSX](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.4/OpenSPIM-1.0.4.dmg)

<details><summary>Click for latest changes:</summary>
<p>

-	Save/load functions for beanshell and java script
-	Added example fusion scripts
-	Supported ClijX in script panel
-	Updated help files
-	Added the citation information in LoadingDialog window
</p>
</details>

3.  In the starting window multiple µManager configuration files can be added, removed and selected. Click *Add .cfg file* to add and then select your working µManager configuration file ending with .cfg. Then click the *Start* button. After loading the hardware µManager should now be ready for use.

## => Continue to [Image acquisition](/micro-openspim_acquisition)
