---
title: µOpenSPIM acquisition controls
layout: page
description: detailed acquisition controls of µOpenSPIM
---
<a href="https://github.com/openspim/micro-OpenSPIM" target="_blank" title="µOpenSPIM-Github Site"><img src="https://openspim.org/images/%C2%B5OS_Logo.png" width="200"></a> 

Go back to [Image acquisition](/micro-openspim_acquisition)

## Acquisition Controls
The following image will introduce you to the location of all available controls to set up an imaging session.</br>
For a more detailed description follow this link: <strong>[Detailed Acquisition controls for µOpenSPIM.](https://openspim.org/images/%C2%B5OpenSPIM_Acquisition_08-03.jpg)</strong>
<figure>
  <a href="https://openspim.org/images/Figure5_Acquisition-panel_website.png" target="_blank" title="µOpenSPIM-Acquisition panel"><img width="1024" src="https://openspim.org/images/Figure5_Acquisition-panel_website_1317x887.png"></a>
<figcaption>Acquisition Controls of the µOpenSPIM GUI (A-I) with the Picard 4D-stage controls on the top right (J) and the Console window on the bottom right  (K). For a higher resolution image click <a href=\images/Figure5_Acquisition-panel_website.png>here.</a>
</figcaption>
</figure>  

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(A)</span> **Positions**</br>
This table shows the list of predefined positions, which will be acquired at each time point. There might be multiple positions or just one. A position is defined by the location where the four motorized stepper motors (X, Y, Z, and R) will move before acquiring an image or stack at a given time point.</br>
In case of an 3-dimensional stack, the Z stage will have three location values: Z start and Z end location values, both defining the total volume of the stack, and the Z step size value, which specifies the total amount of slices within this volume, whereby each slice is one image.

1.  <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add position:</span>&nbsp;Clicking this button will add a row to the end of the table with the current X, Y, Z and R coordinates.
2.  <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Delete position:</span>&nbsp;Clicking this will remove a highlighted row from the table. You can click and drag rows and move them up and down by using the arrows at the end of the row.
3.  <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Update position:</span>&nbsp;Clicking this button will update the selected position according to the current 4D-stage positions (X, Y, Z, R).

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(B)</span> **Define Z-stacks**</br>
Here the beginning and the end of a new stack together with its Z step size can be specified using the Z stage. One has to first find the sample and a centre it in the field of view. By navigating through the sample along the z-axis the beginning and end of a z-stack is specified. 
1. <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Z-start:</span>&nbsp;Clicking this button will mark the current z stepper motor position as the beginning of a desired z-stack.
2. <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Z-end:</span>&nbsp;Clicking this button will mark the current z stepper motor position as the end of a desired z-stack.
3. <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Go to centre:</span>&nbsp;Clicking this button will move the stage Z into the centre of the defined z-stack.
4. <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add Z-stack:</span>&nbsp;Clicking this button will add a row to the end of the positions table that will include the X, Y, and R positions together with the two z-stack positions (Z-start and Z-end) and the Z step size value.</br>
-   It is possible to manually change any positional values by double-clicking on one of the positional entries. Note that this can be done during an ongoing imaging session.
5. <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">New Z-stack:</span>&nbsp;Clicking this button will clear all previously locked Z-stack values in order to define a new Z-stack.</br>
-   It is possible to manually change any positional values by double-clicking on one of the positional entries. Note that this can be done during an ongoing imaging session.

In order to overwrite all positional values with the current positions of the stepper motors simply select any previously created position entry and press the “Update position” button.

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(C)</span> **Time points**</br>
This table includes the information how often the predefined positions should be acquired. A time point can be specified once or many times for long term time lapse recordings. In case 3-d stacks are acquired across a given period of time, the imaging process is referred to as 4d-Microscopy.
1. <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add TP:</span>&nbsp;Clicking this button will add a row to the end of the time points table where the number of time points and their recurrent intervals can be specified.
2. <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add Pause:</span>&nbsp;Clicking this button will add an acquisition break to the end of the time points table. 
3. <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Delete TP:</span>&nbsp;Clicking this will remove any highlighted row from the time points table.

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(D)</span> **Channels**</br>
A typical channel is a laser of a given wavelength illuminating the sample during acquisition. In case an Arduino UNO is in control of one or several lasers, they all must be wired to one of the digital output pins. It is possible that a channel represents a different device other than a laser. Alternatively, lasers can also be controlled by the Software, which in our case is µManager. Do find out more about Software versus Hardware controlled imaging, click [here](/micro-openspim_softwarevshardware).
1. **Software controlled** Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add channel</span>&nbsp;to add a new channel to the table. Several channels can be added to the table. 
-   Click into the drop-down menus to change Camera and the correct Shutter for the intended laser line.
- Double click on the exposure value of any added channel to change it.
2. **Arduino Controlled:** Simply select one or several of the available channels (**Pin8** to **Pin13**) that are under the control of the Arduino-Shutter. Channel Names can be changed in the Arduino UNO configuration table.
    - Double click on the exposure value of any added channel to change it.

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(E)</span> **Summary**</br>
This table provides a summary of the final imaging session with its current settings.

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(F)</span> **Saving options**</br>
1.  <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Save images:</span>&nbsp;If ticked acquired images will be saved to the hard disk. 
2.  &nbsp;<img src="https://openspim.org/images/specify_dir.png" width="20">&nbsp;Clicking this button will allow you to specify an Output directory.
3.  &nbsp;<img src="https://openspim.org/images/open_dir_v2.png" width="20">&nbsp;Clicking this button will open the specified Output folder.
4.  <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Saving format:</span>&nbsp;
    - Choose <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">Single Plane TIFF</span>&nbsp;to save every image individually.
    - Select <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">OMETIFF Image stack</span>&nbsp;to save every time-point as an individual stack including all channels as an ometiff file.
    - Select <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">N5 format</span>&nbsp;to save your acquired data in the N5 format, which allows images to be available in multiple resolutions and can be written in parallel. More info on N5 can be found [here.](https://github.com/saalfeldlab/n5)
5.  <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">Show/save Maximum intensity Projections of each TP:</span>&nbsp;We advise to tick this option for long time-lapse recordings. It can be very useful to have a first impression of how well an imaging session goes or went, particularly if large SPIM data is acquired where generating MIPs after imaging is completed can be very time-consuming.
6.  Here notes can be written down, which will be saved as an additional Note.txt file into the Output directory.

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(G)</span> **Save/Load settings**</br>
All input settings created by the user including Positions, Time points and Channels can be saved here and loaded again at a later time point.
1.  Click <span style="color:#008000; background-color:#DCDCDC; font-weight:bold">SAVE</span>&nbsp;to save all acquisition settings as an .xml file.
2.  Click <span style="color:#FFA500; background-color:#DCDCDC; font-weight:bold">LOAD</span>&nbsp;to load previously saved acquisition settings.
3.  Click <span style="color:#FA8072; background-color:#DCDCDC; font-weight:bold">CLEAR</span>&nbsp;to clear the Acquisition panel from all settings and tables.

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(H)</span> **Acquisition**</br>
After all positions and number of time points have been specified, it's almost time to start imaging. However, there are still a few options worth considering before starting the acquisition process such as ROI, Anti-Drift and Binning. It's also worth checking one more time if the correct saving format has been chosen and whether Maximum Intensity Projections should be generated on the fly.
1. <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">Anti-Drift:</span>&nbsp;Click the Anti-drift tab to enable it with the aim to prevent the sample from leaving its initial predefined position. One can choose between Phase Correlation (whereby entire volume of a 3d-stack is taken into account) or Centre of Mass (whereby drifts are only corrected in x, y but not in z). Note that high concentrations of fluorescent beads surrounding the sample may disarrange the Anti-Drift functionality.
2. <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">Binning:</span>&nbsp;Different binning options can be selected before acquisition, e.g. **2x2** or **3x3** binning. Higher Binning settings combines the charge of more pixels, which increases the signal to noise ratio (SNR) and results in higher camera frame rates but on the expanse of pixel resolution.
3. <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">On-the-fly:</span>&nbsp;On-the-fly will enable the “process()” method of a running script, which can be created or edited within the Java Editor (Editor > Java).
4. <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">ROI:</span>&nbsp;Within this tab a region of interest (ROI) can be specified and applied to the field of view of the camera. The region is specified in the preview window of µManager. Select the Rectangle tool and create a selection inside the preview window. The window will open up by clicking *Live view*. When the ROI is specified, click the <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Apply</span>&nbsp;button.<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Live:</span>&nbsp;Clicking this button will toggle the camera into live view. The exposure values can be changed below.
5. <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Acquire:</span>&nbsp;Clicking this button will start the currently set up imaging session.

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(I)</span> **Preview of imaging session**</br>
Here a simple schematic overview is given showing the current list of time points that have been set up.

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(J)</span> **Stage**</br>
Here you can move the four stepper motors of the 4D-stage Stages (X, Y, Z, R), calibrate the rotational stepper size (R Stage), save and load current positions and inverse the axis of the x and y stage, which might be crucial for the Anti-Drift to work correctly.
    
1.  <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Save current position:</span>&nbsp;Click this button to save the current position of the stage. It will be added to a list.
2.  <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Load location:</span>&nbsp;Click this button to Load a previously saved stage position from a list.
3.  <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">Indicate angles:</span>&nbsp;Indicate here the number of angles you wish to acquire during a single time-point. The angles will then be indicated above the rotational stage (Stage R).
4.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Homing</span>&nbsp;on one of the four Stages to move the stepper motor back to its home position.
5.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Stop</span>&nbsp;to immediately stop a stepper motor.
6.  <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Calibrate:</span>&nbsp;Click this button to calibrate the R Stage in case the 360 degrees do not correspond to a full revolution of the sample holder.
7.  <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add Pos.</span>&nbsp;Clicking this button will add a row to the end of the Position table using the current X, Y, Z and R coordinates.
8.  <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Go back to the last used position</span>&nbsp;Clicking this button will move the stage to the previous position.

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(K)</span> **Console**</br>
The console window can be useful to see what is going on in the background of the plugin and to spot error messages.
1.  Clicking <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Clear</span>&nbsp; will delete all written content.
    
