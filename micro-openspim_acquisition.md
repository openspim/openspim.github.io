<a><img src="https://openspim.org/images/%C2%B5OS_Logo.png" width="200"></a> 

</br>Go back to the [µOpenSPIM starting page](/micro-openspim)</br>

## Getting familiar with µOpenSPIM's GUI
-   The GUI of µOpenSPIM can be arranged in many ways and then saved and restored if needed.</br>
Click <a href=\µOpenSPIM_GUI>here</a> for more information and help.

## Acquisition Controls
The following image will introduce you to the location of the available controls to set up an imaging session.</br>
For more detailed descriptions of the acquisition controls follow this link: <strong>[Detailed Acquisition controls for µOpenSPIM.](/micro-openspim_acquisition-controls)</strong>
<figure align="center">
  <a href="https://openspim.org/images/Figure5_Acquisition-panel_website.png" target="_blank" title="µOpenSPIM-Acquisition panel"><img width="1024" src="https://openspim.org/images/Figure5_Acquisition-panel_website_1317x887.png"></a>
<figcaption>Acquisition Controls of the µOpenSPIM GUI (A-I) with the Picard 4D-stage controls on the top right (J) and the Console window on the bottom right  (K).
</figcaption>
</figure>  

<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(A)</span> **Positions**
<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(B)</span> **Define Z-stacks**
<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(C)</span> **Time points**
<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(D)</span> **Channels**
<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(E)</span> **Summary**
<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(F)</span> **Saving options**</br>
<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(G)</span> **Save/Load settings**
<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(H)</span> **Acquisition**
<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(I)</span> **Preview of imaging session**
<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(J)</span> **Stage**
<span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(K)</span> **Console**

## Acquisition with µOpenSPIM 
The process of acquiring images ranges from snapping a single image to recording overnight (or longer) time lapses of samples from N different angles.

## Acquiring a Single Image
<img src="https://openspim.org/images/µOpenSPIM_single-image.png" width="100"></br>
 To acquire a single image with µOpenSPIM:

1.  Navigate the 4D stage <span style="color:#FF00FF; background-color:#DCDCDC; font-weight:bold">(J)</span> &nbsp;to the location you want to image.
2.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add current position</span>&nbsp;to add this plane to the position list. 
3.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add TP</span>&nbsp;and set both, the number of time points (TP) and the interval, to 1.
4.  Add at least one channel to the Software Controlled Channels list or select one of the Channels that are available in the Arduino Controlled Channels list. Don't forget to set the desired exposure time of each channel.
5.  You may specify an Output directory&nbsp;<img src="https://openspim.org/images/specify_dir.png" width="20">&nbsp;if you would prefer the image be written straight to disk, rather than opened in µManager using the computer memory. A metadata.txt file of all acquisition settings will also be saved into the Output directory.
6.  Finally, click <span style="color:#008000; background-color:#DCDCDC; font-weight:bold">Acquire</span>&nbsp;to capture a single or multi-channel image.

## Acquiring a Stack
<img src="https://openspim.org/images/µOpenSPIM_single-stack.png" width="100"></br>
A stack is a sandwich of many image slices of different focus levels of the sample with a defined beginning and end. To set up a stack requires to move the Z stage.

1.  Navigate to the sample location where the Z stack should begin.
2.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Z-start</span>&nbsp;and the current Z position will now show up next to the button.
3.  Navigate to the sample location where the stack should end.
4.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Z-end</span>&nbsp; and the current Z position swill show up once again next to the button.
5.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Go to centre</span>&nbsp;and check if the Z Stage ends up in the middle of the stack. This is a good way to know that the Z stack has been set correctly.
6.  Specify the Z-Step Size (in μm).
7.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add Pos.</span>&nbsp;to add the newly defined Z stack to the position list on the left. It will also include the X, Y, and R positions.
8.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add TP</span>&nbsp;and set both, the number of time points (TP) and the interval, to 1.
9.  Add at least one channel (either Software Controlled or Arduino Controlled) to the Channels list and set each channel's exposure time.
10. Though a single stack can easily fit into the memory, it is recommended that you specify an Output directory&nbsp;<img src="https://openspim.org/images/specify_dir.png" width="20">&nbsp;so the stack is saved to the disk. A metadata file of all acquisition settings will additionally be saved into the Output directory.
11. Optionally:
    -   turn on <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">Show/Save Maximum Intensity Projections of each TP</span>&nbsp;to receive a Maximum Intensity Projection (MIP) after the stack has been fully acquired. The MIP will be saved into its own sub-folder within the Output directory.
12. Click <span style="color:#008000; background-color:#DCDCDC; font-weight:bold">Acquire</span>&nbsp;to capture the defined stack.

## Single-Plane Time Lapse
<img src="https://openspim.org/images/µOpenSPIM_time-lapse.png" width="300"></br>
 To acquire a time lapse of a single plane, set up the recording exactly as if you were going to record only one image.

1.  After clicking <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add TP</span>&nbsp;specify how often the plane should be imaged and set its recurring time interval (in seconds, minutes, hours or days).
    - Optionally you can add acquisition breaks by clicking <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add Pause</span>. Then specify the length of the acquisition break and click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add TP</span>&nbsp;to continue with a new time lapse recording after the acquisition break.
2.  Add at least one channel (either Software Controlled or Arduino Controlled) to the Channels list and set each channel's exposure time.
3.  &nbsp;<img src="https://openspim.org/images/specify_dir.png" width="20">&nbsp;Clicking this button will allow you to specify an Output directory. A metadata file of all acquisition settings will additionally be saved into the Output directory.
4.  Optionally:
    -   Enable Anti-Drift: choose between Phase Correlation (functionality is based on the 3d-stack with x, y, and z coordinates) or Centre of Mass (functionality is only based on x, y coordinates). Note that beads surrounding the sample might affect the Anti-Drift.
    -   Enable Binning: Choose one of the binning options and press apply.
    -   Enable On-the-fly: This will enable the “process()” method of a running script, which can be created or edited within the Java Editor (Editor > Java). You can give it a try by running the "ClijxMaxFusionDoG" example script located within the Java Editor. Press "Run" to execute it and make sure the "On-the-fly" box in the Acqusiiton panel is ticked. The example script will fuse [(maximumImages)](https://clij.github.io/clij2-docs/reference_maximumImages), substract background of the fused stack [(differenceOfGaussian3D)](https://clij.github.io/clij2-docs/reference_differenceOfGaussian3D) and create a MIP [(maximumZProjection)](https://clij.github.io/clij2-docs/reference_maximumZProjection). The three operations take place on the graphics processing unit (GPU) using the GPU-accelerated image processing library [(CLIJ2)](https://clij.github.io/) and the three output files will be saved into the specified output directory into a subfolder called "output". Make sure you specify the correct number of channels inside the script before you start aciring images.
    -   Select a region of interest (ROI): Select a ROI with the Rectangle tool in the µManager's preview window, which will pop up when you click *Live View*. Then click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Apply</span>.

5.  Click <span style="color:#008000; background-color:#DCDCDC; font-weight:bold">Acquire</span>&nbsp;to begin the time-lapse recording.

## Single-View Time Lapse
<img src="https://openspim.org/images/µOpenSPIM_4d-time-lapse.png" width="300"></br>
 To record a single view/stack of a sample over time:

1.  Navigate the 4D-stage to the location you wish to acquire images and specify the beginning and the end of the Z stack and the Z-Step Size (in μm) as described above. In the Picard 4D-stage the minimum Z step size is 1.524 µm. 
2.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add Pos.</span>&nbsp;to add the newly defined Z stack to the position list on the left and specify how often the stack should be imaged and set the recurring time interval (in seconds, minutes, hours or days).
3.  &nbsp;<img src="https://openspim.org/images/specify_dir.png" width="20">&nbsp;Clicking this button will allow you to specify an Output directory. A metadata file of all acquisition settings will additionally be saved into the Output directory.
4.  Optionally:
    - Enable Anti-Drift: choose between Phase Correlation (functionality is based on the 3d-stack with x, y, and z) or Centre of Mass (functionality based on x, y). Note that beads surrounding the sample might affect the Anti-Drift.
    - Select a Region of interest (ROI): Select a ROI with the Rectangle tool in the µManager's preview window, which will pop up when you click *Live View*. Then click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Apply</span>.
    - Enable Binning: Choose one of the binning options and press apply.
    - Turn on <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">Show/Save Maximum Intensity Projections of each TP</span>&nbsp;to receive a Maximum Intensity Projection (MIP) after the stack has been fully acquired. The MIP will be saved into its own subfolder within the Output directory.
5.  Click <span style="color:#008000; background-color:#DCDCDC; font-weight:bold">Acquire</span>&nbsp;to begin the multi-view time-lapse recording.

## Multi-View Time Lapse
<img src="https://openspim.org/images/µOpenSPIM_multiview-timelapse.png" width="300"></br>
To record multiple views of a sample over time:

1.  For each view:
    - Navigate the 4D-stage to the location you wish to acquire images.
    - Specify the beginning and the end of the Z stack and the Z-Step Size (in μm) as described above. In the Picard 4D-stage the minimum Z step size is 1.524 µm. 
    - Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add Pos.</span>&nbsp;to add the newly defined Z stack to the position list on the left.
2.  After clicking <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add Pos.</span>&nbsp;specify how often the stack(s) or view(s) should be imaged and set the recurring time interval (in seconds, minutes, hours or days).  Add acquisition breaks by clicking <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add Pause</span>&nbsp;and specify its length. Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add TP</span>&nbsp;to add new time lapse span which will continue after the acquisition break.
3.  &nbsp;<img src="https://openspim.org/images/specify_dir.png" width="20">&nbsp;Clicking this button will allow you to specify an Output directory. A metadata file of all acquisition settings will additionally be saved into the Output directory.
4.  Optionally:
    - Enable Anti-Drift: choose between Phase Correlation (functionality is based on the 3d-stack with x, y, and z) or Centre of Mass (functionality based on x, y). Note that beads surrounding the sample might affect the Anti-Drift.
    - Select a Region of interest (ROI): Select a ROI with the Rectangle tool in the µManager's preview window, which will pop up when you click *Live View*. Then click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Apply</span>.
    - Enable Binning: Choose one of the binning options and press apply.
    - Turn on <span style="color:#000000; background-color:#DCDCDC; font-weight:bold">Show/Save Maximum Intensity Projections of each TP</span>&nbsp;to receive a Maximum Intensity Projection (MIP) after the stack has been fully acquired. The MIP will be saved into its own subfolder within the Output directory.
5.  Click <span style="color:#008000; background-color:#DCDCDC; font-weight:bold">Acquire</span>&nbsp;to begin the multi-view time-lapse recording.