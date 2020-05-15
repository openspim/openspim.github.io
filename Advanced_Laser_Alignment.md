---
---
This page will walk you through aligning the light sheet from scratch.
It is recommended that the detection axis be installed before putting
the optics into place.

# Preparation

This step will prepare you for a complete system realignment. This may
take up to several hours, so be sure you have enough time to devote to
the task.

1.  If there are any refractive optics in the illumination path, remove
    them now. The illumination axis should only have:
    1.  A 2-mirror beam walk in front of the laser,
    2.  A corner mirror,
    3.  and an optical slit (presently widened to maximum).
2.  Complete a very-rough laser alignment: The beam emitted by the laser
    should strike the approximate center of each mirror in the path,
    ending at the center of the illumination objective.

# Initial Alignment

During this step, we will align the beam with the optical axis and get
its waist focused on the detection axis.

1.  Walk the laser directly down the first segment of the optical axis.
    1.  Insert two beam alignment disks at the beginning and end of the
        long, 300mm rail. Make sure there is as much distance between
        the two of them as possible.
          - Any alignment disk with a center hole will do; the parts
            list calls for frosted glass disks (DG05-1500-H1-MD), but
            you could also use LMR1AP on 1" mounts with the appropriate
            stilt, or even two irises adjusted very narrow.
    2.  Use the *first* mirror to position the beam in the center of the
        *first* alignment disk. (Depending on how close the first disk
        is to the second mirror, adjusting the second mirror will have
        considerably less effect -- *but not none*\!)
    3.  Use the *second* mirror to position the beam in the center of
        the *second* alignment disk.
    4.  Optimize both mirrors simultaneously to ensure the beam is
        running parallel at 50mm off the breadboard down the center of
        the illumination axis.
2.  Align the second segment of the optical axis.
    1.  Move your alignment disks to the beginning and end of the
        smaller, second-segment rail. One disk should be directly
        against the sample chamber, while the other should be very close
        to the corner mirror.
    2.  Adjust the corner mirror to run the beam directly between the
        centers of both disks.
        1.  **If the corner mirror is on a kinematic mount:** You may
            need to turn all three knobs a considerable amount to
            position the point of beam reflection onto both segments of
            the illumination path. Then adjust the horizontal and
            vertical knobs to orient the beam correctly. This may bear
            repetition, since adjusting these knobs does not rotate the
            mirror through the point at which the beam reflects\!
        2.  **If the corner mirror is on a gimbal mount:** You may need
            to loosen the rail carrier holding the mount and adjust it
            along the 45-degree rail so the beam bounces off the center
            of the mirror. Then adjust the horizontal and vertical knobs
            to orient the beam correctly. Although the horizontal
            position on the mirror should remain centered, it is
            possible that the vertical position will shift slightly; as
            a result, you may need to repeat this process.
3.  View and adjust the beam.
    1.  Make the beam visible to the camera.
        1.  Fill the sample chamber with water, then activate the
            software and open the live view.
        2.  Raise the laser power to approx. 15 mW, and the exposure to
            around 100 ms.
        3.  If you cannot identify the beam in the live view, try
            adjusting the corner mirror's vertical component -- the
            motion may help your eyes pick out the borders of the beam.
        4.  On the main Micro-Manager window, find a good contrast
            setting and make sure **Autostretch** option is unchecked.
    2.  Add a 'reticle' to the live view.
        1.  Using ImageJ/Fiji's *Edit -\> Selection -\> Specify...*,
            enter half of the image's pixel width and height in the X
            and Y coordinates and check *Centered*.
        2.  Enter a reasonable width/height for the box to form a
            nicely-sized rectangle (try 500 x 100).
        3.  If desired, use *Image -\> Overlay -\> Add Selection...* to
            convert the ROI to an overlay. (However, the handles may be
            helpful to show half-points on the box -- and by extension,
            the entire image.)
    3.  Use the corner mirror's horizontal adjustment to focus the beam
        in the center of the image.
          - Turning this knob will appear to move the beam waist
            (narrowest point) left and right.
          - Realigning this mirror now may lead to better results, but
            if the adjustment is not too significant, it is optional.
    4.  Use the corner mirror's vertical adjustment to center the beam
        along the image's height.
          - Turning this knob will appear to move the entire beam up and
            down.
          - Again, consider realigning the second segment of the optical
            axis.

<!-- end list -->

  - At this point you should have a conic shape, with diffraction
    limited waist in the center of the view.
  - If the beam seems to need an angle adjustment, it may indicate that
    the first segment of the axis is not properly aligned.

# First Beam Expander and Intermediate Adjustment

During this step, we'll install the first refractive optics, then
compensate for their changes to the beam path.

1.  [Install the beam
    expander.](Install_illumination_axis_on_the_optical_breadboard_-_Part_2#Assembling_the_beam_expander "wikilink")
    1.  Realign the first segment of the optical axis -- the refractive
        optics will have changed the beam's endpoint slightly. Refer to
        the above instructions for details.
2.  View and adjust the beam again.
    1.  This time, the beam waist's *horizontal location* is decided by
        *the distance between the two lenses*.
        1.  Adjust this distance until the beam waist is centered on the
            image.
        2.  Then turn the corner mirror's horizontal knob until the
            waist is as sharp and bright as possible.
        <!-- end list -->
          - The distance between lenses affects how collimated the
            outgoing beam is. A perfectly collimated beam will be
            focused to the illumination objective's focal point, while a
            converging or diverging beam will focus before or after this
            point, respectively.
    2.  The vertical adjustment is the same as above: use the corner
        mirror's vertical knob to center the beam waist vertically on
        the image.

<!-- end list -->

  - In this step and the next, to achieve the best possible alignment
    would theoretically require 'walking' the corner mirror whenever it
    would be adjusted, in particular if this mirror is on a kinematic
    mount: any adjustment moves the point-of-incidence of the beam, thus
    moving it off the optical axis.
      - In practice, these changes are often slight enough that this
        adjustment can be overlooked.

# Second Beam Expander and Final Rough Pass

During this step, we'll put in the second two-lens system and again
compensate for their influence on the beam.

1.  [Install the BFP lens
    system.](Install_illumination_axis_on_the_optical_breadboard_-_Part_2#Assembling_the_telescope "wikilink")
    1.  Realign the second segment of the optical axis. Note that the
        position of the second lens may make it difficult to put in the
        far alignment disk; if so, be careful about adjusting the corner
        mirror, or you may lose the beam in the live view.
2.  View and adjust the beam again.
    1.  Restore the horizontal centering.
          - Again, the beam waist's horizontal location will be affected
            by the lens spacing. You may need to move both mirrors to
            keep the objective's back focal plane aligned with the
            second lens' forward focal plane.
    2.  Once this is done, use the corner mirror's horizontal adjustment
        to optimize the beam waist.
    3.  Restore the vertical centering (same as above).

<!-- end list -->

  - After this step, you can replace the cylindrical lens on the optical
    axis. Although it should be focused on the corner mirror, and the
    first lens of the second (BFP) system should have a focal point in
    the same place, this doesn't seem to be an absolute requirement --
    the position of the cylindrical lens makes little apparent
    difference.
  - Once the cylindrical lens is in place, the view through the live
    window will be mostly useless: you will be looking at a sheet of
    light, parallel to the camera's chip.
      - However, physical inspection of the sample chamber should show
        the sheet sharply narrowing near the center of the field of
        view, then expanding to as many as two or three centimeters on
        the far side of the chamber.

# Light Sheet Refinement and Characterization

In this step, we'll observe the light sheet directly and finish
adjusting it, then measure its width.

**Important:** At this point, make sure you have an appropriate
combination of filters in the combined optical path. Directing laser
light onto the camera's CCD is can permanently damage the camera.

  - The infinity space should contain a filter blocking the laser's
    primary emission wavelength. A band-stop or long-pass filter at the
    appropriate wavelength will suffice.
  - It may be necessary to *remove* any cleanup filters in the
    illumination path.
      - These filters remove all light except the laser's primary
        wavelength, which the later filter will block.
      - For viewing the light sheet directly, these secondary
        wavelengths are actually very useful: they are emitted at a
        lower power than the primary light, and may pass through the
        detection filters.

<!-- end list -->

1.  Turn off the laser.
      - This can be done by disabling its power supply, setting the
        laser power to 0, or 'closing' Micro-Manager's shutter (disable
        auto-shutter).
2.  Set up the alignment sample.
    1.  We assume herein that the alignment sample is a fragment of a
        light-microscope alignment slide, with a partial or complete
        grid, and an intact mirrored section spanning the camera's field
        of view.
    2.  Insert the sample with the mirrored face facing the camera. Make
        it as parallel to the camera as possible.
    3.  Using the software, move the stage to focus on the grid.
    4.  Adjust the angle until the grid lines are equally out of focus
        across the camera's field of view.
          - It may help to focus on the grid in between angular
            adjustments: look for sections of grid lines growing
            unfocused as they progress to the left or right.
          - Optionally zero the rotational motor; this way, the
            following rotation is as simple as entering (-)45 in the
            stage controls window.
              - This function is not yet implemented in the OpenSPIM
                software, but may be performed using the Picard Twister
                control software. It is safe to do this while
                MM/OpenSPIM is running.
    5.  Rotate the stage 45 degrees to reflect the laser light down the
        detection axis.
          - Be careful the rotation is in the correct direction. Watch
            the sample as you rotate it through 45 degrees and make sure
            the mirrored surface is now 45 degrees between the two
            objective lenses.
    6.  Refocus on one of the grid lines. The grid to the left and right
        of center will be unfocused; this is expected as the grid's
        surface is no longer parallel to the focal plane.
3.  Step the laser up in power slowly, until the light sheet is visible.
      - Try 0.1 mW steps, starting from 0.5 mW. OpenSPIM 1.0's 488nm
        Cube gives best results at around 0.91 mW. (The second decimal
        place may not display, but the Coherent Cube recognizes it
        correctly.)
4.  Adjust the corner mirror's horizontal controls to center the sheet
    on the center of the image.
      - It may be useful to create a reticle as before, but with the
        height and width swapped to give a vertical rectangle.
5.  Adjust the final lens in the sequence back and forth along its rail
    to focus the light sheet.
      - Keep an eye on the 'max' statistic in Micro-Manager. If you
        begin to saturate the camera, lower the laser power and/or
        reduce the exposure.
      - The first beam expander also contributes to the focus, and may
        require fine-tuning.
6.  The light sheet diverges in either direction from the middle; the
    vertical slit must be narrowed to counteract this.
    1.  Take a Z- or X- stack of the mirror surface and observe the
        beam's divergence at the edges of the field of view.
    2.  Narrow the vertical slit until the light sheet is reasonably
        consistent across the camera's view.
          - As the slit narrows, the centered beam will widen and lose
            amplitude.

<!-- end list -->

  - You'll have to make a qualitative judgment about the consistency of
    the light-sheet vs. its width. A narrow slit will cause a wider
    light sheet, but it won't change as dramatically across the view of
    the camera.
  - Keep in mind that if the light sheet is very wide at the edges of
    the view, this will illuminate out-of-focus parts of the sample.

# TODO

1.  Add pictures of expected results at important locations.
