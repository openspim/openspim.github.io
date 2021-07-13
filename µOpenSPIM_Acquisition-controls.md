## Acquisition Controls
<figure>
  <img src="https://openspim.org/images/%C2%B5OpenSPIM_Acquisition.jpg" width="1024">
<figcaption>Acquisition Controls of the µOpenSPIM GUI (A-I) with the Picard 4D-stage controls on the top right (J) and the Console window on the bottom right  (K). For a higher resolution image click <a href=\images/%C2%B5OpenSPIM_Acquisition.jpg>here</a>.

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

  - (E) Preview of imaging session</br>
  This is a simple schematic overview of the current time points table. Nothing can be specified here.

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