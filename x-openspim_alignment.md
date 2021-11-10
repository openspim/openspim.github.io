## Alignment guide X-OpenSPIM
There are different ways how to optimally align an OpenSPIM system and it can take time to get the hang of it. With two illumination sides and two detection objectives this task becomes particularly challenging. This site provides a simple, reproducible way of how to 
-   initially align the beam along the rails
-   visualize and tune the beam within the field of view of the cameras 
-   align the created light-sheet on the sample (final step).

## Requirements
-   Make sure appropriate laser safety measures and training has been carried out and that µManager’s “Hardware configuration wizard” has been completed for at least one camera, one laser and the USB-4D stage.
-   A syringe to mount a glass capillary into the acquisition chamber. The capillary should be filled with agarose containing any fluorescent beads, which can be exited by the laser in use.

## How to set up µManager before using µOpenSPIM?
-   Click [here](/micro-openspim_micromanager-configuration) if you have never created a working .cfg file with µManager before or/and want to get guidance on configuring multiple cameras, pixel size calibration and configuring an ArduinoUNO board for µManager.

## Installation and start-up of µOpenSPIM
-   Right now, µOpenSPIM is in its beta stage and works with µManager 2.0.1 20210721 for Windows (nightly build 21 July 2021).
-   See also our [µOpenSPIM-Github Site](https://github.com/openspim/micro-OpenSPIM).

## Acquiring a Single Image
<img src="https://openspim.org/images/µOpenSPIM_single-image.png" width="100"></br>
 To acquire a single image with µOpenSPIM:

1.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add current position</span>&nbsp;to add this plane to the position list. 
2.  Finally, click <span style="color:#008000; background-color:#DCDCDC; font-weight:bold">Acquire</span>&nbsp;to capture a single or multi-channel image.
