## 2. Visualizing and tuning the beam within the field of view of one or two cameras
After the alignment along the rails carrying the optical components is completed, the emitted laser beam can be visualized in agarose and adjusted by slightly changing the positions of the spherical lens assemblies along the rails.
<details><summary>Preparations:</summary>
<p>
-   Prepare 1% water agarose containing fluorescent beads (e.g., 1:2000), which fit the laser excitation and emission filters of your OpenSPIM system. Sonicate the beads in a 1:100 stock solution for 3 min before mixing them with water agarose or vigorously vortex it for several minutes to avoid clustering.</br>
-   Vortex the Agarose containing the beads for 3 min and soak it into a glass capillary e.g., by using a plunger. In case of an X-OpenSPIM we recommend to already mount some kind of sample, which can be easily spotted. For detailed descriptions for mounting and preparing samples visit the <a href="https://openspim.org/Sample_Preparation">OpenSPIM website</a>.
<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure7.png" target="_blank"><img width="700" src="https://openspim.org/images/alignment/Alignment_Figure7.png"></a>
<figcaption> Figure 7 - Glass capillary containing agarose that can be pushed out using a plunger (left) and mounted glass capillary depicted in the center of the acquisition chamber, which has been filled with water.
</figcaption>
</figure>  

-   Fill the acquisition chamber with water, mount and find the lower edge of the glass capillary using any available bright light source (even the torch of your phone can be used). Then push out the agarose by gently pressing the plunger until the column of agarose can easily cover the entire field of view. Make sure the glass capillary is completely out of view.</br>
</p>
</details>

<details><summary>Click here in case a second camera is used</summary>
<p>
For the first time the focal plane of both detection objectives within the fields of view of both sister cameras can now be coaligned by focusing the second camera onto the exact same spot (e.g., the bottom left or right edge of the capillary or some kind of recognizable spot or sample) to which the first camera already points. Alignment is achieved by gently sliding the detection objective forward and backward along the detection axis using the plastic handle that connects to the objective holder ring of the detection objective (see the [chamber modifications of the X-OpenSPIM acquisition chamber](https://openspim.org/table_of_parts_xopenspim)). At the same time the corner mirror mount knobs (KCB2EC/M, Thorlabs) installed in on of the detection axes have to be adjusted to bring the two fields of views closer together (see also Figure 12). Ensure that both sister cameras have the same top and bottom orientation and try to make the best possible overlap of both cameras.</br></br>
</p>
</details>

<span style="color:darkred; font-weight:bold">Attention! Particularly in an X-OpenSPIM setup with two detection objectives, it is crucial that the glass capillary with its column of agarose is positioned well in the center of the chamber before proceeding with the alignment!</span>&nbsp;
Use the 4D-stage to focus on the left or right edge of the agarose and center the column of agarose in the field of view.

<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure8.png" target="_blank"><img width="700" src="https://openspim.org/images/alignment/Alignment_Figure8.png"></a>
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
</br>__In case a second camera is used:__</br>
Once both illumination sides are aligned and the beam is clearly visible within the column of agarose in one of the two cameras (using no cylindrical lenses and no emission filters), then the detection objective of the second camera should be adjusted up to the point where the beams of both detection axes are highly similar in shape and clearly visible as demonstrated in Fogure 9, C.</br>

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 11</span>&nbsp;
Adjust the vertical gimbal mount adjuster knob (Number 2 in Figure 9, E) to center the beam. In this way both illumination paths are aligned and centered in the field of view until they overlap each other.

<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure9.png" target="_blank"><img width="700" src="https://openspim.org/images/alignment/Alignment_Figure9.png"></a>
<figcaption> Figure 9 - Visualizing and aligning the laser beam within the field of view. Insets (A-D) show actual pictures captured in the field of view of one of the two cameras. A) Broad beam of the left illumination before adjusting the horizontal gimbal mount knob of the corner mirror. B) Correct alignment of one of the two 
illumination beams C) illumination beam with a slight misalignment (shift) to the left of its focal point. D) One of the illumination beams needs to be
adjusted with the vertical gimbal mount adjuster knob to center it in the field of view. E) 1 = horizontal gimbal mount adjuster knob; 2 = vertical gimbal mount adjuster knob; 3 = telescopic lenses; 4 = plastic handles that connect to the objective holder ring of their respective  detection objective and are used to slide the objective along the detection axis.
</figcaption>
</figure>  

<span style="color:#1E90FF; background-color:#DCDCDC; font-weight:bold">Step 12</span>&nbsp;
Check if any rotational misalignment between the field of view of both sister cameras is visible. An example of this can be seen in Figure 10 (see inset).  If this is the case, one camera has to be rotated (Figure 10, red double-arrow) until the mismatch is corrected.

<figure align="center">
  <a href="https://openspim.org/images/alignment/Alignment_Figure10.png" target="_blank"><img width="700" src="https://openspim.org/images/alignment/Alignment_Figure10.png"></a>
<figcaption> Figure 10 - Rotating one of the two sister cameras may be necessary to match the field of view. The inset depicts a rotational misalignment of Camera 1 of an otherwise aligned beam that has been visualized in agarose after removing emission filters and the cylindrical lenses.
</figcaption>
</figure>  