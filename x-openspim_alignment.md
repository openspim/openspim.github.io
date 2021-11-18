## Alignment guide X-OpenSPIM
There are different ways how to optimally align an OpenSPIM system and it can take time to get the hang of it. With two illumination sides and two detection objectives, as it is the case in an [X-OpenSPIM](https://openspim.org/table_of_parts_xopenspim), this task becomes particularly challenging. This site aims to provide a simple, reproducible way of how to...
-   (1) initially align the beam path along the rails
-   (2) visualize and tune the beam within the field of view of one or two cameras 
-   (3) fine align the created light-sheet on the sample (final step).

## Requirements
-   Make sure appropriate laser safety measures and training has been carried out and that µManager’s “Hardware configuration wizard” has been completed for at least one camera, one laser and the USB-4D stage.
-   A syringe to mount a glass capillary into the acquisition chamber. The capillary should be filled with agarose containing any fluorescent beads, which can be exited by the laser in use.

## 1. Aligning the laser beam along the rails
For the alignment along the rails, which carry the optical components of the first and second telescope system, we use mirrors (BB05-E02, Thorlabs) mounted on kinematic mounts (KM05/M, Thorlabs) and a corner mirror mounted on a gimbal mirror mount. Note that the corner mirror is a modification of the original OpenSPIM design and is placed on its own short rail piece that was cut off from a 300 mm optical rail (RLA300/M, Thorlabs).
All mirrors placed into a kinematic mount should be adjusted to approximately 45 degrees to ensure a perpendicular bounce of the beam. After the alignment the emitted laser beam will hit roughly the center of all mirrors and ends at the center of the illumination objective. To achieve this, two separate reference points are needed at the correct height. In a typical OpenSPIM setup the beam would be elevated 50 mm off the surface of the breadboard. For the reference points one can use e.g., nearly closed iris apertures (SM1D12D, Thorlabs), alignment disks (DG05-1500-H1-MD, Thorlabs) or alignment disks created via alignment plates (LMR1AP) for lens mounts (LMR1/M). We used the latter placed on 1" rail carriers (RC1, Thorlabs) to create both reference points at the correct height. In the following the two reference points will be called AD1 and AD2 respectively.

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 1</span>&nbsp;
Remove any optical parts from the illumination axis except for the kinematic mirrors and the corner mirror. If available, place a density filter (e.g., OD: 2.0) close to the exit face of the laser housing and set laser intensity to a minimum. The beam should be barely visible to the eye for safety reasons.

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 2</span>&nbsp;
Adjust the beam splitter cube and aim for two beams that are perpendicular to each other when they hit the first two kinematic mirrors.

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 3</span>&nbsp;
Now adjust all kinematic mounts until the laser beam roughly follows the desired path along the optical rails (see Figure 1 below).
<figure style="font-weight:italic"; align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure1.png" target="_blank"><img width="900" src="https://openspim.org/images/alignment/Alignment_Figure1.png"></a>
<figcaption> Figure 1 - Aligning the laser along the rails by adjusting the Kinematic Mirrors (KM) with their mounts set to 45 degrees along the rails (red arrows). The two blue arrows point to the fine adjustment screws of the kinematic mount. The perpendicular beam path branching off the beam splitter easily tilts to one side (yellow dotted line), which should be avoided.
</figcaption>
</figure>  
Try to find the central spot of each KM as indicated in Figure 2.
This requires some patience, because in order to achieve a perpendicular bounce, kinematic mirrors have to be taken off the breadboard, then readjusted (slightly turned) by loosening and tightening their rail carriers, and then placed back on the optical breadboard and into the beam path. This typically requires several attempts. Ensure that the laser hits approximately the center of each mirror and try to avoid using the fine adjustment screws too much. They need to have sufficient margin in the next step and should retain a more or less neutral position.
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure2.png" target="_blank"><img width="500" src="https://openspim.org/images/alignment/Alignment_Figure2.png"></a>
<figcaption> Figure 2 - Centering the beam on the kinematic mirrors
</figcaption>
</figure>  

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 4</span>&nbsp;
Place the first alignment disc at the beginning of the first optical rail and the second alignment disc at its end. Adjust the kinematic mounts (KM05/M, Thorlabs) of the reflecting mirrors.
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure3.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure3.png"></a>
<figcaption> Figure 3
</figcaption>
</figure>  
Start with the first kinematic mirror (KM1) using the fine adjustment screws (pink arrows) and aim for the central opening of the first alignment disc (AD1). Then adjust the second kinematic mirror (KM2, green arrows) but this time try to hit the central hole of the second alignment disc (AD2). The laser beam will not hit the alignment disc right away. Instead, it typically diminishes before reaching the central hole of the alignment disc. Whenever this is the case, go back to the first kinematic mirror (KM1) and readjust for the Iris aperture hole. Play this back and forward until the beam strikes both reference points and the first optical rail is correctly aligned.
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure4.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure4.png"></a>
<figcaption> Figure 4
</figcaption>
</figure>  

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 5</span>&nbsp;
Proceed to the second optical rail between the corner mirror and the illumination objective of the chamber. Again, place the two reference points at the beginning and the end of the rail. Initially the Gimbal mount knobs of the corner mirror should be brought into a neutral position and the first alignment done by sliding the corner mirror forward or backward along the rail. There should be a reasonable alignment of the beam before fixing the mirror onto the rail. Now the beam can be aligned by adjusting the corner mirror with the horizontal and vertical adjuster knobs of the Gimbal mounts until the beam passes directly through the center of both alignment disc holes.
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure5.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure5.png"></a>
<figcaption> Figure 5
</figcaption>
</figure>  

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 6</span>&nbsp;
Mount the lenses of the first telescope system (without the cylindrical lens) and pay attention that the distance between them roughly equals the sum of their focal length (19 mm and 75 mm means that the distance between the two lenses should be 94 mm). Note that by placing the telescopic lenses, the beam has significantly expanded. Follow the enlarged beam starting behind the telescopic lenses e.g., with a piece of cleaning tissue, and check if the beam retains the same diameter until it hits the corner mirror. This indicates that the distance between the two lenses is correct.  It may be a good idea to verify if the telescopic lenses did not severely alter the alignment of the laser e.g., by placing an alignment plate at the end of the rail. Such misalignments can be avoided by ensuring that the telescopic lenses are tightly assembled and that the lens mounts face the illumination axis without any tilt. One might need to make minor adjustments using the screws of the kinematic mounts to correct for small deviations of the beam caused by the inserted lenses.
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure6.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure6.png"></a>
<figcaption> Figure 6
</figcaption>
</figure>  

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 7</span>&nbsp;
Repeat step 1-6 to align a possible second illumination axis.

## 2. Visualizing and tuning the beam within the field of view of one or two cameras
Now that the alignment along the rails carrying the optical components is completed, the emitted laser beam can be visualized in agarose after adding the two telescope systems and adjusted by slightly changing the positions of the spherical lens assemblies along the rails.
Preparations:
-   Prepare 1% water agarose containing fluorescent beads (e.g., 1:2000), which fit the laser excitation and emission filters of your OpenSPIM system. Sonicate the beads in a 1:100 stock solution for 3 min before mixing them with water agarose or vigorously vortex it for several minutes to avoid clustering.
-   Vortex the Agarose containing the beads for 3 min and soak it into a glass capillary e.g., by using a plunger. For detailed descriptions for mounting and preparing samples visit the [OpenSPIM website](https://openspim.org/Sample_Preparation).
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure7.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure7.png"></a>
<figcaption> Figure 7
</figcaption>
</figure>  

-   Fill the acquisition chamber with water, mount and find the lower edge of the glass capillary using any available bright light source (even the torch of your phone can be used). Then push out the agarose by gently pressing the plunger until the column of agarose covers the entire field of view. Make sure the glass capillary completely out of view. Now focus on the left or right edge of the Agarose and center the column of agarose in the field of view. Particularly in an X-OpenSPIM with two detection objectives, it is important that the glass capillary with the Agarose is positioned well in the center of the chamber before proceeding with the alignment.

<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure8.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure8.png"></a>
<figcaption> Figure 7
</figcaption>
</figure>  

## 3. Fine align the created light-sheet on the sample
