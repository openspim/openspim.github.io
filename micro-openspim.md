
<a href="https://github.com/openspim/micro-OpenSPIM" target="_blank" title="µOpenSPIM-Github Site"><img src="https://openspim.org/images/%C2%B5OS_Logo.png" width="200"></a> is an intuitive new graphical user interface (GUI) for OpenSPIM users, which relies on [µManager](https://micro-manager.org).

## Features of µOpenSPIM
-   A complete overhaul of the GUI has been made including simple graphic visualizations and an improved control over Picrard’s 4D-stage
-   A user-friendly way of setting up multiview time lapse recordings with several positions and the option to acquire periodic and sporadic intervals with optional breaks during time-lapse recordings
-   A quick save function for nearly all acquisitions settings to save time in case an imaging session is interrupted or a similar session will take place at another time
-   Different saving formats allow acquisition as single plane tiff files, whole stacks or in n5 format, which is optimised for browsing through big data.
-   ArduinoUNO support for basic but efficient control of several connected hardware devices so that OpenSPIM users can quickly benefit from improved image acquisition speed and acquisition accuracy
-   An option for on-the-fly maximum intensity projections
-   A Picard Stage calibration feature to correct rotational inaccuracies and to improve the 4D-USB stage control
-   A tested drift-correction functionality with new options that can help with keeping a drifting sample within the field of view during long term image acquisition
- And more to come...

## µOpenSPIM requirements
-   All hardware components of an OpenSPIM system (Laser, Camera, Stage, etc.) have to be pre-configured with µManager's Hardware Configuration Wizard using Version 2.0 gamma (nightly build 04 May 2021) on a Windows7/10 computer.
-   µOpenSPIM has been tested with Picard's USB 4D-Stage in mind. Using different 4D-Stages should work but could lead to unexpected behaviour.

## How to set up µManager before using µOpenSPIM?
-   Click [here](/micro-openspim_micromanager-configuration) if you have never created a working .cfg file with µManager before or/and want to get guidance on configuring multiple cameras, pixel size calibration and configuring an ArduinoUNO board for µManager.

## Installation and start-up of µOpenSPIM
-   Right now, µOpenSPIM is in its beta stage and works with µManager 2.0.1 20210721 for Windows (nightly build 21 July 2021).
-   See also our [µOpenSPIM-Github Site](https://github.com/openspim/micro-OpenSPIM).
1.  Please [download](https://valelab4.ucsf.edu/~MM/builds/2.0/Mac/Micro-Manager-2.0.0.dmg) and install the [64-bit](https://valelab4.ucsf.edu/~MM/nightlyBuilds/2.0/Windows/MMSetup_64bit_2.0.1_20210721.exe) build of [µManager](https://micro-manager.org/) and follow its *Hardware Configuration Wizard* to create a functional configuration file (.cfg) that allows µManager to control the OpenSPIM hardware. On the first time startup of µOpenSPIM users will be asked to select the file location of µManager.
2.  __Download µOpenSPIM__ for <strong>[Windows 64-bit](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.3/OpenSPIM_setup_1.0.3.exe)</strong> or <strong>[MacOSX](https://github.com/openspim/micro-OpenSPIM/releases/download/v1.0.3/OpenSPIM-1.0.3.dmg)</strong> and follow the installation guide.

3.  In the starting window multiple µManager configuration files can be added, removed and selected. Click *Add .cfg file* to add and then select your working µManager configuration file ending with .cfg. Then click the *Start* button. After loading the hardware µManager should now be ready for use.

## [=> Getting Started with μOpenSPIM / Image acquisition](/micro-openspim_acquisition)
