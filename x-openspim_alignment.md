## Alignment guide X-OpenSPIM
There are different ways how to optimally align an OpenSPIM system and it can take time to get the hang of it. With two illumination sides and two detection objectives this task becomes particularly challenging. This site provides a simple, reproducible way of how to...
-   initially align the beam along the rails
-   visualize and tune the beam within the field of view of the cameras 
-   align the created light-sheet on the sample (final step).

## 1. Requirements
-   Make sure appropriate laser safety measures and training has been carried out and that µManager’s “Hardware configuration wizard” has been completed for at least one camera, one laser and the USB-4D stage.
-   A syringe to mount a glass capillary into the acquisition chamber. The capillary should be filled with agarose containing any fluorescent beads, which can be exited by the laser in use.

## 2. Aligning the laser beam along the rails
For the alignment along the rails, which carry the optical components of the first and second telescope system, we use mirrors (BB05-E02) mounted on kinematic mounts (KM05/M) and a corner mirror mounted on a gimbal mirror mount. Note that the corner mirror is a modification of the original OpenSPIM design and is placed on its own short rail piece that was cut off from a 300 mm optical rail (RLA300/M, Thorlabs).
All mirrors placed into a kinematic mount should be adjusted to approximately 45 degrees to ensure a perpendicular bounce of the beam. After the alignment the emitted laser beam will hit roughly the center of all mirrors and ends at the center of the illumination objective. To achieve this, two separate reference points are needed at the correct height. In a typical OpenSPIM setup the beam would be elevated 50 mm off the surface of the breadboard. For the reference points one can use e.g., nearly closed iris apertures (SM1D12D, Thorlabs), alignment disks (DG05-1500-H1-MD, Thorlabs) or alignment plates (LMR1AP) for lens mounts (LMR1/M). We used the latter placed on 1" rail carriers (RC1, Thorlabs) to create both reference points at the correct height.

-   <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 1</span>&nbsp;
Remove any optical parts from the illumination axis except for the kinematic mirrors and the corner mirror. If available, place a density filter (e.g., OD: 2.0) close to the exit face of the laser housing and set laser intensity to a minimum. The beam should be barely visible to the eye for safety reasons.

-   <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 2</span>&nbsp;
Adjust the beam splitter cube and aim for two beams that are perpendicular to each other when they hit the first two kinematic mirrors.

-   <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 3</span>&nbsp;
Now adjust all kinematic mounts until the laser beam roughly follows the desired path along the optical rails.
</br><img src="https://openspim.org/images/Alignment/Alignment_Figure1.png" width="100"></br>




## Installation and start-up of µOpenSPIM
-   Right now, µOpenSPIM is in its beta stage and works with µManager 2.0.1 20210721 for Windows (nightly build 21 July 2021).
-   See also our [µOpenSPIM-Github Site](https://github.com/openspim/micro-OpenSPIM).

## Acquiring a Single Image
<img src="https://openspim.org/images/µOpenSPIM_single-image.png" width="100"></br>
 To acquire a single image with µOpenSPIM:

1.  Click <span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Add current position</span>&nbsp;to add this plane to the position list. 
2.  Finally, click <span style="color:#008000; background-color:#DCDCDC; font-weight:bold">Acquire</span>&nbsp;to capture a single or multi-channel image.
