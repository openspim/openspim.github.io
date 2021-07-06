
<img src="https://openspim.org/images/%C2%B5OS_Logo.png" width="200"> is an intuitive new graphical user interface (GUI) for OpenSPIM users, which relies on [µManager.](https://micro-manager.org)

## Features of µOpenSPIM
-   A complete overhaul of the GUI has been made including simple graphic visualizations and an improved control over Picrard’s 4D-stage.
-   A user-friendly way of setting up multiview time lapse recordings with several positions and the option to acquire periodic and sporadic intervals with optional breaks during time-lapse recordings.
-   A quick save function for nearly all acquisitions settings to save time in case an imaging session is interrupted or a similar session will take place at another time.
-   Arduino UNO support for basic but efficient control of several connected hardware devices so that OpenSPIM users can quickly benefit from improved image acquisition speed and acquisition accuracy.
-   An option for on-the-fly maximum intensity projections
-   A Picard Stage calibration feature to correct rotational inaccuracies and to improve the 4D-USB stage control
-   A tested Anti-drift logic similar to the old plugin but with new options that can help with keeping a drifting sample within the field of view during long term image acquisition.
- And more to come...

## Installation and start-up of the µOpenSPIM
-   Right now µOpenSPIM is in its beta stage and works with µManager gamma1 20210504 for Windows (nightly build 04 May 2021).
1.  Please download and install the [64-bit](https://valelab4.ucsf.edu/~MM/nightlyBuilds/2.0.0-gamma/Windows/MMSetup_64bit_2.0.0-gamma1_20210504.exe)or [32-bit](https://valelab4.ucsf.edu/~MM/nightlyBuilds/2.0.0-gamma/Windows/MMSetup_32bit_2.0.0-gamma1_20210504.exe)build of [µManager](https://micro-manager.org/)and follow its *Hardware Configuration Wizard* to create a functional configuration file (.cfg) that allows µManager to control the OpenSPIM hardware. On the first time startup of µOpenSPIM users will be asked to select the file location of µManager.
2.  <strong>[Download](https://openspim.org/%C2%B5OpenSPIM)</strong>and unzip the µOpenSPIM folder into any directory and start the application using the *µOpenSPIM.exe* file.
3.  CLick the *START* button (top left). In the new window multiple µManager configuration files can be added, removed and selected. Click *Add .cfg file* to add and then select your working µManager configration file ending with .cfg. Then click the *Start* button. After loading the hardware µManager should now be ready for use.

## Getting familiar with µOpenSPIM's GUI.
-   The GUI of µOpenSPIM can be arranged in many ways and then saved and restored if needed.
Follow this link to see a demonstration of [one possible way to arrange the GUI of µOpenSPIM.](https://openspim.org/videos/Arrange-GUI.mp4)
[<img src="https://openspim.org/images/µOpenSPIM_change-GUI.png" width="750">](https://openspim.org/videos/Arrange-GUI.mp4)

## Acquisition with µOpenSPIM 
The process of acquiring images ranges from snapping a single image to recording overnight (or longer) time lapses of samples from N different angles.

## Acquiring a Single Image
<img src="https://openspim.org/images/µOpenSPIM_single-image.png" width="100">
 To acquire a single image with µOpenSPIM:

1.  Navigate the 4D stage to the location you want to image.
2.  Click *Add current position* to add this plane to the position list. 
3.  Click *Add TP* and set both, the number of time points (TP) and the interval, to 1.
4.  Add at least one channel to the Software Controlled Channels list or select one of the Channels that are available in the Arduino Controlled Channels list. Don't forget to set the desired exposure time of each channel.
5.  You may specify an Output directory if you would prefer the image be written straight to disk, rather than opened in µManager using the computer memory. A metadata.txt file of all acquisition settings will also be saved into the Output directory.
6.  Finally, click *Acquire* to capture a single or multi-channel image.

## Acquiring a Stack
<img src="https://openspim.org/images/µOpenSPIM_single-stack.png" width="100">
A stack is a sandwich of many image slices of different focus levels of the sample. To set up a stack requires to move the Z stage.

1.  Navigate to the sample location where the Z stack should begin.
2.  Click *Z-start*. The current Z position will now show up next to the button.
3.  Navigate to the sample location where the stack should end.
4.  Click *Z-end*. The current Z position swill show up once again next to the button.
5.  Click *Go to centre* and check if the Z Stage ends up in the middle of the stack. This is a good way to know that the Z stack has been set correctly.
6.  Specify the Z-Step Size (in μm).
7.  Click *Add Pos.* to add the newly defined Z stack to the position list on the left. It will also include the X, Y, and R positions.
8.  Click *Add TP* and set both, the number of time points (TP) and the interval, to 1.
9.  Add at least one channel (either Software Controlled or Arduino Controlled) to the Channels list and set each channel's exposure time.
10. Though a single stack can easily fit into the memory, it is recommended that you specify an Output directory so the stack is saved to the disk. A metadata file of all acquisition settings will additionally be saved into the Output directory.
11. Optionally, turn on *Show/Save Maximum Intensity Projections of each TP* to receive a Maximum Intensity Projection (MIP) after the stack has been fully acquired. The MIP will be saved into its own subfolder within the Output directory.
12. Click *Acquire* to capture the defined stack.

## Single-Plane Time Lapse
<img src="https://openspim.org/images/µOpenSPIM_time-lapse.png" width="300">
 To acquire a time lapse of a single plane, set up the recording exactly as if you were going to record only one image.

1.  After clicking *Add TP* specify how often the plane should be imaged and set its recurring time interval (in seconds, minutes, hours or days).
    - Optionally you can add acquisition breaks by clicking *Add Pause*. Then specify the length of the acquisition break and click *Add TP* to continue with a new time lapse recording after the acquisition break.
2.  Add at least one channel (either Software Controlled or Arduino Controlled) to the Channels list and set each channel's exposure time.
3.  Specify an Output directory. A metadata file of all acquisition settings will additionally be saved into the Output directory.
4.  Optionally:
    a) Enable Anti-Drift: choose between Phase Correlation (logic is based on the 3d-stack with x, y, and z coordinates) or Centre of Mass (logic is only based on x, y coordinates). Note that beads surrounding the sample might affect the Anti-Drift.
    b) Select a region of interest (ROI): Select a ROI with the Rectangle tool in the µManager's preview window, which will pop up when you click *Live View*. Then click *Apply*.
    c) Enable Binning: Choose one of the binning options and press apply.
5.  Click *Acquire* to begin the time-lapse recording.

## Single-View Time Lapse
<img src="https://openspim.org/images/µOpenSPIM_4d-time-lapse.png" width="300">
 To record a single view/stack of a sample over time:

1.  Navigate the 4D-stage to the location you wish to acquire images and specify the beginning and the end of the Z stack and the Z-Step Size (in μm) as described above. In the Picard 4D-stage the minimum Z step size is 1.524 µm. 
2.  Click *Add Pos.* to add the newly defined Z stack to the position list on the left and specify how often the stack should be imaged and set the recurring time interval (in seconds, minutes, hours or days).
3.  Specify an Output directory. A metadata file of all acquisition settings will additionally be saved into the Output directory.
4.  Optionally:
    - a) Enable Anti-Drift: choose between Phase Correlation (logic is based on the 3d-stack with x, y, and z) or Centre of Mass (logic based on x, y). Note that beads surrounding the sample might affect the Anti-Drift.
    - b) Select a Region of interest (ROI): Select a ROI with the Rectangle tool in the µManager's preview window, which will pop up when you click *Live View*. Then click *Apply*.
    - c) Enable Binning: Choose one of the binning options and press apply.
    - d) Turn on *Show/Save Maximum Intensity Projections of each TP* to receive a Maximum Intensity Projection (MIP) after the stack has been fully acquired. The MIP will be saved into its own subfolder within the Output directory.
5.  Click *Acquire* to begin the multi-view time-lapse recording.

## Multi-View Time Lapse
<img src="https://openspim.org/images/µOpenSPIM_multiview-timelapse.png" width="300">

To record multiple views of a sample over time:

1.  For each view:
    - a)  Navigate the 4D-stage to the location you wish to acquire images.
    - b)  Specify the beginning and the end of the Z stack and the Z-Step Size (in μm) as described above. In the Picard 4D-stage the minimum Z step size is 1.524 µm. 
    - c)  Click *Add Pos.* to add the newly defined Z stack to the position list on the left.
2.  After clicking *Add TP* specify how often the stack(s) or view(s) should be imaged and set the recurring time interval (in seconds, minutes, hours or days).  Add acquisition breaks by clicking *Add Pause* and specify its length. Click *Add TP* to add new time lapse span which will continue after the acquisition break.
3.  Specify an Output directory. A metadata file of all acquisition settings will additionally be saved into the Output directory.
4.  Optionally:
    - a) Enable Anti-Drift: choose between Phase Correlation (logic is based on the 3d-stack with x, y, and z) or Centre of Mass (logic based on x, y). Note that beads surrounding the sample might affect the Anti-Drift.
    - b) Select a Region of interest (ROI): Select a ROI with the Rectangle tool in the µManager's preview window, which will pop up when you click *Live View*. Then click *Apply*.
    - c) Enable Binning: Choose one of the binning options and press apply.
    - d) Turn on *Show/Save Maximum Intensity Projections of each TP* to receive a Maximum Intensity Projection (MIP) after the stack has been fully acquired. The MIP will be saved into its own subfolder within the Output directory.
5.  Click *Acquire* to begin the multi-view time-lapse recording.


## Acquisition Controls
<figure>
  <img src="https://openspim.org/images/%C2%B5OpenSPIM_Acquisition.jpg" width="1024">
<figcaption>Acquisition Controls of the µOpenSPIM GUI (A-I) with the Picard 4D-stage controls on the top right (J) and the Console window on the bottom right  (K). For a higher resolution image click <a href=\images/%C2%B5OpenSPIM_Acquisition.jpg>here.</a>

</figcaption>
</figure>  

  - (A) Positions  
    This table shows the list of stacks of images to acquire. Each time point will consist of the images recorded at each position in this list (as well as the Z slices described by the range in the Z column).
    1.  Add position
        - Clicking this button will add a row to the end of the table with only the current position. In case a z-stack is not defined a single slice will be taken at the given location.
    2.  Delete position
        - Clicking this will remove any currently-highlighted rows from the table. You can click and drag rows or move them up and down with the arrows at the end of the row.
    3.  Update position: Update selected position according to the current 4D-stage positions (X, Y, Z, R).

  - (B) Define Z-stacks
    1. Z-start
        - Clicking this button will mark the current z stepper motor position as the beginning of a desired z-stack.
    2. Z-end
        - Clicking this button will mark the current z stepper motor position as the end of a desired z-stack.
    3. Go to centre
        - Clicking this button will move the stage Z into the centre of the defined z-stack.
    4. Add Pos.
        - Clicking this button will add a row to the end of the positions table that will include the X, Y, and R positions as well as the two z-stack positions (Z-start and Z-end).  

  - (C) Time points (TP)
    1. Add TP
        - Clicking this button will add a row to the end of the time points table where the number of time points and their recurrent intervals can be specified.
    2. Add Pause
        - Clicking this button will add an acquisition break to the end of the time points table. 
    3. Delete TP
        - Clicking this will remove any currently-highlighted rows from the time points table.

  - (D) Acquisition
    1. Acquire
        - Clicking this button will start the specified imaging session.
    2. Anti-Drift
        - Clicking the Anti-drift tab and enabling it will be an attempt to prevent the sample from leaving its initial position. Users can choose between Phase Correlation (whole 3d-stack is taken into account) or Centre of Mass (drifts are only corrected in x, y). Be careful, as high concentrations of fluorescent beads surrounding the sample may disarrange the Anti-Drift.
    3. ROI
        - This is where a region of interest (ROI) can be applied. But first a ROI has to be specified in the preview window of µManager. To do so, select the Rectangle tool and make a selection within the preview window. The preview window will open up by clicking *Live view*. The Live view can be stopped while using the Rectangle tool.
    4. Binning
        - Here different binning options can be selected for the acquisition, e.g. 2x2 or 3x3 binning. Binning combines the charge of pixels, which increases the signal to noise ratio (SNR) and leads to higher camera frame rates but on the expanse of pixel resolution. 

  - (E) Preview of imaging session
        - This is a simple schematic overview of the current time points table. Nothing can be specified here.

  - (F) Select Channels/Pins
        - Add one or more "channels". A channel is typically a laser but it can also be another hardware component of the OpenSPIM. There are two ways of controlling a channel during acquisition: 1) Software controlled (without an ArduinoUNO microcontroller) and 2) Arduino Controlled (with an ArduinoUNO microcontroller). 
    1. Software controlled:
        - Click *Add channel* to add a new channel to the table. Click into the drop-down menus to change e.g. the Shutter of a laser. Several channels can be added to the table.
        - Double click onto the existing Exposure number to change the exposure time of a given channel.
    2. Arduino Controlled:
        -  Simply select one or several of the available channels that are under the control of the Arduino-Shutter. Channel Names can be changed in the Arduino Uno configuration table.
  
  - (G) Saving options
    1.  Save images 
        - If ticked acquired images will be saved to the hard disk. 
    2.  Clicking this button will allow you to specify an Output directory.
    3.  Clicking this button will open the specified Output folder.
    4.  Saving format:
        - Choose *Single Plane TIFF* to save every image individually.
        - Select *OMETIFF Image stack* to save every time-point as an individual stack including all channels.
        - Select *N5 format* to save your acquired data in the N5 format, which allows images to be available in multiple resolutions and can be written in parallel. More info on N5 can be found here: https://github.com/saalfeldlab/n5.
    5.  Show/save Maximum intensity Projections of each TP.
        - We advise to tick this option for long time-lapse recordings. It can be very useful to have a first impression of how well an imaging session goes or went, particularly if large SPIM data is acquired where generating MIPs after imaging is completed can be very time-consuming.
    6.  Here notes can be written down, which will be saved as an additional Note.txt file into the Output directory.

  - (H) Summary
    This table provides a summary of the final imaging session with its current settings.

  - (I) Acquisition Settings
        - All settings including Positions, Time points and Channel/Pins tables can be saved here.
    1.  Click *SAVE* to save all acquisition settings as an .xml file.
    2.  Click *LOAD* to load previously saved acquisition settings.
    3.  Click *CLEAR* to clear the Acquisition panel from all settings and tables.

  - (J) Stage
        - Move the four Stages (X, Y, Z, R) and calibrate the rotational stepper size (R Stage) and the Anti-Drift.
    1.  Save current position
        - Click this button to save the current position of the stage. It will be added to a list.
    2.  Load location
         - Click this button to Load a previosly saved stage position from a list.
    3.  Indicate angles
        - Indicate here the number of angles you wish to acquire during a single time-point. The angles will then be indicated above the rotational stage (Stage R).
    4.  Calibrate
        - Click this button to calibrate the R Stage in case the 360 degrees do not correspond to a full revolution of the sample holder.
    5.  Click *Homing* on one of the four Stages to move the stepper motot back to its home position.
    6.  Click *Stop* to immediately stop a stepper motor.

  - (K) Console
        - The console window can be useful to see what is going on in the background of the plugin and to spot error messages.
    1.  Clicking *Clear* will delete all written content.
    
