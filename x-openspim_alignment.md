## Welcome to the OpenSPIM alignment guide!

There are different ways how to optimally align an OpenSPIM system and it can take time to get the hang of it. With two illumination sides and two detection objectives, as it is the case in an [X-OpenSPIM](https://openspim.org/table_of_parts_xopenspim), this task becomes particularly challenging. This site aims to provide a simple, reproducible way of how to...
-   (1) initially align the beam path along the rails
-   (2) visualize and tune the beam within the field of view of one or two cameras 
-   (3) fine align the light-sheet for the sample using beads.

The alignment guide was initially written for a recent [X-OpenSPIM publication](https://onlinelibrary.wiley.com/doi/10.1002/adbi.202101182) but can be applied in almost the same way to the L, and T-OpenSPIM configuration.</br>
Renderings have been created by Charlène Brillard [(Tomancak Group)](https://www.mpi-cbg.de/research-groups/current-groups/pavel-tomancak/group-members/).

## Requirements
-   Make sure appropriate laser safety measures and training has been carried out and that µManager’s “Hardware configuration wizard” has been completed for at least one camera, one laser and the USB-4D stage.
-   A syringe to mount a glass capillary into the acquisition chamber. The capillary should be filled with agarose containing any fluorescent beads, which can be exited by the laser in use.
-   In case of an X-OpenSPIM acquisition chamber modifications are needed to allow additional adjustments of the detections objectives (see chamber parts [here](https://openspim.org/table_of_parts_xopenspim)) 

## 1. Aligning the laser beam along the rails
For the alignment along the rails, which carry the optical components of the first and second telescope system, one can use Ø1/2" mirrors (BB05-E02, Thorlabs) mounted on kinematic mounts (KM05/M, Thorlabs) and larger Ø1" corner mirrors (BB1-E02, Thorlabs) mounted on gimbal mirror mounts (GM100/M, Thorlabs). Note that the corner mirror is a modification of the original OpenSPIM design and is placed on its own short rail piece that was cut off from a 300 mm optical rail (RLA300/M, Thorlabs).
All mirrors placed into a kinematic mount should be adjusted to approximately 45 degrees to ensure a perpendicular bounce of the beam. After the alignment the emitted laser beam will hit roughly the center of all mirrors and ends at the center of the illumination objective. To achieve this, two separate reference points are needed at the correct height. In a typical OpenSPIM setup the beam would be elevated 50 mm off the surface of the breadboard. For the reference points one can use e.g., nearly closed iris apertures (SM1D12D, Thorlabs), alignment disks (DG05-1500-H1-MD, Thorlabs) or alignment disks created via alignment plates (LMR1AP) for lens mounts (LMR1/M). We used the latter placed on 1" rail carriers (RC1, Thorlabs) to create both reference points at the correct height. In the following the two reference points will be called AD1 and AD2 respectively.

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 1</span>&nbsp;
Remove any optical parts from the illumination axis except for the kinematic mirrors (see Figure 1). If available, place a density filter (e.g., OD: 2.0) close to the exit face of the laser housing and set laser intensity to a minimum. The beam should be barely visible to the eye for safety reasons.

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 2</span>&nbsp;
Adjust the beam splitter cube and aim for two beams that are perpendicular to each other when they hit the first two kinematic mirrors.

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 3</span>&nbsp;
Now adjust all kinematic mounts until the laser beam roughly follows the desired path along the optical rails (see Figure 1 below).
<figure style="font-weight:italic"; align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure1.png" target="_blank"><img width="900" src="https://openspim.org/images/alignment/Alignment_Figure1.png"></a>
<figcaption> Figure 1 - Aligning the laser along the first optical rail by adjusting the Beam Splitter and Kinematic Mirrors (KM1-KM3) with their mounts set to 45 degrees along the rails as shown on the right. The two blue arrows point to the fine adjustment screws of the kinematic mount, which will be used later. The perpendicular beam path branching off the Beam Splitter easily tilts to one side (see yellow dotted line), and should be avoided. Red double headed arrows indicate adjustment direction.
</figcaption>
</figure>  
Try to find the central spot of each KM as indicated in Figure 2.
This requires some patience, because in order to achieve a perpendicular bounce, kinematic mirrors have to be taken off the breadboard, then readjusted (slightly turned as shown in Figure 1, side view of KM) by loosening and tightening their rail carriers, and then placed back on the optical breadboard and into the beam path. This typically requires several attempts. Ensure that the laser hits approximately the center of each mirror and try to excessive use the fine adjustment screws as they need to have sufficient margin in Step 4 and should for now retain a more or less neutral position.
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure2.png" target="_blank"><img width="500" src="https://openspim.org/images/alignment/Alignment_Figure2.png"></a>
<figcaption> Figure 2 - The beam has been correctly centered on the kinematic mirrors.
</figcaption>
</figure>  

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 4</span>&nbsp;
Place the first alignment disc at the beginning of the first optical rail and the second alignment disc at its end as depicted in Figure 3. Now readjust the kinematic mounts (KM05/M, Thorlabs) of the reflecting mirrors until the beam hits the central hole of the first reference point (AD1) and the central spot of all kinematic mirrors.
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure3.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure3.png"></a>
<figcaption> Figure 3 - Two reference points (AD1 and AD2) have been created on the first optical rail.
</figcaption>
</figure>  
Start with the first kinematic mirror (KM1) using the fine adjustment screws (pink arrows) and aim for the central opening of the first alignment disc (AD1). Then adjust the second kinematic mirror (KM2, green arrows) but this time try to hit the central hole of the second alignment disc (AD2). The laser beam will not hit the alignment disc right away. Instead, it typically diminishes before reaching the central hole of the alignment disc. Whenever this is the case, go back to the first kinematic mirror (KM1) and readjust for the Iris aperture hole. Play this back and forward until the beam strikes both reference points and the first optical rail is correctly aligned.
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure4.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure4.png"></a>
<figcaption> Figure 4 - Beam alignment along the first optical rail.
</figcaption>
</figure>  

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 5</span>&nbsp;
Proceed to the second optical rail between the corner mirror and the illumination objective of the chamber. Again, place the two reference points at the beginning and the end of the rail (see Figure 5). Initially the Gimbal mount knobs of the corner mirror should be brought into a neutral position and the first alignment done by sliding the corner mirror forward or backward along the rail (Figure 5, red double headed arrow). There should be a reasonable alignment of the beam before tightly fixing the mirror onto the rail. Now the beam can be aligned by adjusting the corner mirror with the horizontal (H) and vertical (V) adjuster knobs of the Gimbal mounts until the beam passes directly through the center of both alignment disc holes.
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure5.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure5.png"></a>
<figcaption> Figure 5 - Beam alignment along the second optical rail.
</figcaption>
</figure>  

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 6</span>&nbsp;
Mount the lenses of the first telescope system as shown in Figure 6 (without the cylindrical lens) and make sure that the distance between them roughly equals the sum of their focal length (e.g., 19 mm and 75 mm means that the distance between the two lenses should be 94 mm as depicted in Figure 6). Note that by placing the first two telescopic lenses (19 mm and 75 mm), the beam significantly expands. Follow the enlarged beam starting behind the 75 mm telescopic lens (a piece of lens cleaning tissue will do) and check if the beam retains the same diameter along the rails until it hits the corner mirror. At this point it may be a good idea to verify whether the insertion of the telescopic lenses did not severely alter the alignment of the laser beam. This can be checked by placing an alignment disk at the end of the rail. Such misalignment are common and can be avoided by ensuring that the telescopic lenses are tightly assembled and that the lens mounts face the illumination axis without any tilt. One might need to make minor adjustments using the screws of the kinematic mounts to correct for small deviations of the beam caused by the inserted lenses.
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure6.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure6.png"></a>
<figcaption> Figure 6 - The beam is aligned along all rails for the first illumination sides.
</figcaption>
</figure>  

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 7</span>&nbsp;
Repeat step 1-6 to align a possible second illumination axis.

## 2. Visualizing and tuning the beam within the field of view of one or two cameras
Now that the alignment along the rails carrying the optical components is completed, the emitted laser beam can be visualized in agarose and adjusted by slightly changing the positions of the spherical lens assemblies along the rails.
Preparations:
-   Prepare 1% water agarose containing fluorescent beads (e.g., 1:2000), which fit the laser excitation and emission filters of your OpenSPIM system. Sonicate the beads in a 1:100 stock solution for 3 min before mixing them with water agarose or vigorously vortex it for several minutes to avoid clustering.
-   Vortex the Agarose containing the beads for 3 min and soak it into a glass capillary e.g., by using a plunger. In case of an X-OpenSPIM we recommend to already mount some kind of sample, which can be easily spotted. For detailed descriptions for mounting and preparing samples visit the [OpenSPIM website](https://openspim.org/Sample_Preparation).
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure7.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure7.png"></a>
<figcaption> Figure 7 - Glass capillary containing agarose that can be pushed out using a plunger (left) and mounted glass capillary depicted in the center of the acquisition chamber, which has been filled with water.
</figcaption>
</figure>  

-   Fill the acquisition chamber with water, mount and find the lower edge of the glass capillary using any available bright light source (even the torch of your phone can be used). Then push out the agarose by gently pressing the plunger until the column of agarose can easily cover the entire field of view. Make sure the glass capillary is completely out of view.
</br>
**In case a second camera is used:**</br>
Now is the time to coalign for the first time the focal plane of both detection objectives within the fields of view of both sister cameras by focusing the second camera onto the exact same spot (e.g., the bottom left or right edge of the capillary or some kind of recognizable spot or sample) to which the first camera already points. Alignment is achieved by gently sliding the detection objective forward and backward along the detection axis using the plastic handle that connects to the objective holder ring of the detection objective (see the [chamber modifications of the X-OpenSPIM acquisition chamber](https://openspim.org/table_of_parts_xopenspim)). At the same time the corner mirror mount knobs (KCB2EC/M, Thorlabs) installed in on of the detection axes have to be adjusted to bring the two fields of views closer together (see also Figure 12). Ensure that both sister cameras have the same top and bottom orientation and try to make the best possible overlap of both cameras.
</br>
<span style="color:darkred; font-weight:bold">Particularly in an X-OpenSPIM setup with two detection objectives, it is crucial that the glass capillary with its column of agarose is positioned well in the center of the chamber before proceeding with the alignment!</span>&nbsp;
Now use the 4D-stage to focus on the left or right edge of the agarose and center the column of agarose in the field of view.

<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure8.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure8.png"></a>
<figcaption> Figure 8 - The glass capillary is positioned in the center of the chamber and a smartphone used as a bright light source to find the capillary and to bring it into the field of view of the camera using the 4D-stage.
</figcaption>
</figure>  

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 8</span>&nbsp;
Remove emission filters and cylindrical lenses on the illumination axes used for alignment and slightly adjust the distance between the 25 mm and 50 mm telescopic lenses and their distance to the illumination objective (Number 3 in Figure 9, E. Try tightening the two telescopic lenses with the spring-loaded plunger of the rail carrier up to the point where they can barely glide along the optical rail (Figure 9, red double headed arrows). At some point the laser beam will become visible, first as an indistinct broad fuzzy beam crossing the field of view horizontally from left to right.
Further adjust the telescope lenses to increase the sharpness of the beam until it looks similar to the one depicted in Supplementary Figure 9, A.

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 9</span>&nbsp;
Adjust the horizontal gimbal mount knob of the corner mirror (Number 1 in Figure 9, E) to bring the illumination beam in focus with the working distance of the detection objective up to the point where it can be seen as a very thin stripe instead of a coarse beam (see Figure 9, B). At this point it often becomes obvious that the focal point of the beam is not centered in the field of view. This shift is shown in Figure 9, C. Again, carefully adjust one of the telescopic lenses (Number 3 in Figure 9) by gently gliding it along the optical rail to correct for this shift (red double headed arrows).

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 10</span>&nbsp;
Repeat step 4 to 6 on the second illumination axis until the left and right illumination beams are aligned and resemble the aligned beam depicted in Figure 9, B.

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 11</span>&nbsp;
Adjust the vertical gimbal mount adjuster knob (Number 2 in Figure 9, E) to center the beam. In this way both illumination paths are aligned and centered in the field of view until they overlap each other.

<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure9.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure9.png"></a>
<figcaption> Figure 9 - Visualizing and aligning the laser beam within the field of view. Insets (A-D) show actual pictures captured in the field of view of one of the two cameras. A) Broad beam of the left illumination before adjusting the horizontal gimbal mount knob of the corner mirror. B) Correct alignment of one of the two 
illumination beams C) illumination beam with a slight misalignment (shift) to the left of its focal point. D) One of the illumination beams needs to be
adjusted with the vertical gimbal mount adjuster knob to center it in the field of view. E) 1 = horizontal gimbal mount adjuster knob; 2 = vertical gimbal mount adjuster knob; 3 = telescopic lenses; 4 = plastic handles that connect to the objective holder ring of their respective  detection objective and are used to slide the objective along the detection axis.
</figcaption>
</figure>  

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 12</span>&nbsp;
Check if any rotational misalignment between the field of view of both sister cameras are visible. An example of this can be seen in Figure 10 (see inset).  If this is the case one camera has to be rotated (Figure 10, red double-arrow) until the mismatch is corrected.

<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure10.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure10.png"></a>
<figcaption> Figure 10 - Rotating one of the two sister cameras may be necessary to match the field of view. The inset depicts a rotational misalignment of Camera 1 of an otherwise aligned beam that has been visualized in Agarose after removing emission filters and the cylindrical lenses.
</figcaption>
</figure>  

## 3. Fine alignment of the light-sheet for the sample using beads
<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 13</span>&nbsp;
Place the cylindrical lenses on the rail and put back the emission filter. Make sure the cylindrical lens is in its correct place and its rotational mount is well adjusted by checking whether a focused, horizontal laser stripe has appeared on the corner mirror surface.

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 14</span>&nbsp;
The correct alignment of both excitation light-sheets can now be tested on fluorescent beads. For this, use the horizontal gimbal mount knob to bring the light-sheet into the focal plane of one of the detection objectives, while simultaneously gently playing with the rotation mount of the cylindrical lens. The beads embedded in agarose should now become focused and visible and ideally cover the field of view homogeneously as small bright dots as shown in the inset of Figure 11.

<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure11.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure11.png"></a>
<figcaption> Figure 11 - Visualizing the beads using the horizontal gimbal mount knob and adjusting the scaled rotation of the cylindrical lens mount (red double headed arrows). Inset shows illuminated and aligned beads of both detection axes (not yet aligned) spreading over the entire field of view. 
</figcaption>
</figure> 

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 15</span>&nbsp;
Different light intensities of the beads between the left and right illumination axes, may indicate slight beam alignment differences. This issue can be corrected by looking at the beads. In the illumination axis, where a lower intensity of beads is observed, the height of the beam can carefully be adjusted by using the two reflecting mirrors positioned prior to the rail carrying the first telescopic system. By making slight adjustments with a 5/64" hex key adjuster, intensities should increase and decrease. Aim to maximize light intensity on both illumination axes.

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 16</span>&nbsp;
An overlap of the field of view of the two sister cameras can be achieved mechanically by looking at beads and using the fine adjustments of the corner mirror mount knobs of one of the detection axes.
First make sure the same beads are visible in the two sister cameras and that the beads are co-focused by moving one of the detection objectives in z. Then use the corner mirror mount knobs (Figure 12, white arrows) of the 2-inch corner mirror mount (KCB2EC/M, Thorlabs) to co-align the two field of views until all beads overlap. If a significant stronger mismatch of beads is visible at the outer corners of the field of view and the impression of a spiraling feeling occurs while going through the beads in z, then one of the two cameras has to be rotated before the overall match of the beads can be improved (see Step 12).

<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure12.png" target="_blank"><img width="800" src="https://openspim.org/images/alignment/Alignment_Figure12.png"></a>
<figcaption> Figure 12 - Corner mirror present in one of the two detection axes to mechanically align the two camera views by using the two mirror mount knobs (white arrows). Inset shows how alignment took place using fluorescent beads.
</figcaption>
</figure> 

The alignment of your OpenSPIM is now completed!

