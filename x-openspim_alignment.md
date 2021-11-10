## Alignment guide X-OpenSPIM
-   A complete overhaul of the GUI has been made including simple graphic visualizations and an improved control over Picrard’s 4D-stage
-   A user-friendly way of setting up multiview time lapse recordings with several positions and the option to acquire periodic and sporadic intervals with optional breaks during time-lapse recordings

## µOpenSPIM requirements
-   All hardware components of an OpenSPIM system (Laser, Camera, Stage, etc.) have to be pre-configured with µManager's Hardware Configuration Wizard using Version 2.0 gamma (nightly build 04 May 2021) on a Windows7/10 computer.
-   µOpenSPIM has been tested with Picard's USB 4D-Stage in mind. Using different 4D-Stages should work but could lead to unexpected behaviour.

## How to set up µManager before using µOpenSPIM?
-   Click [here](/micro-openspim_micromanager-configuration) if you have never created a working .cfg file with µManager before or/and want to get guidance on configuring multiple cameras, pixel size calibration and configuring an ArduinoUNO board for µManager.

## Installation and start-up of µOpenSPIM
-   Right now, µOpenSPIM is in its beta stage and works with µManager 2.0.1 20210721 for Windows (nightly build 21 July 2021).
-   See also our [µOpenSPIM-Github Site](https://github.com/openspim/micro-OpenSPIM).

## Acquiring a Single Image
<img src="https://openspim.org/images/µOpenSPIM_single-image.png" width="100"></br>
 To acquire a single image with µOpenSPIM:

1.  Navigate the 4D stage to the location you want to image.
2.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add current position</span>&nbsp;to add this plane to the position list. 
3.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add TP</span>&nbsp;and set both, the number of time points (TP) and the interval, to 1.
4.  Add at least one channel to the Software Controlled Channels list or select one of the Channels that are available in the Arduino Controlled Channels list. Don't forget to set the desired exposure time of each channel.
5.  You may specify an Output directory&nbsp;<img src="https://openspim.org/images/specify_dir.png" width="20">&nbsp;if you would prefer the image be written straight to disk, rather than opened in µManager using the computer memory. A metadata.txt file of all acquisition settings will also be saved into the Output directory.
6.  Finally, click <span style="color:#008000; background-color:#DCDCDC; font-weight:bold">Acquire</span>&nbsp;to capture a single or multi-channel image.
