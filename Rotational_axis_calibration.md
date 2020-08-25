---
---
Setting your twister angle to 0 before starting will simplify the second part below. Find a convenient bead in the live window and click Calibrate on the OpenSPIM plugin.

## Pixel Size

The top pane helps determine pixel size, and has to be filled out before you can use the bottom pane. Using the bead you have, drag a box with one corner in the approximate center. Move the stage a known amount in X and Y -- using the arrow keys is advised as each press is 10 motor steps. Align the opposite corner of the ROI rectangle on the bead's new position, then click the Pick ROI button. It should change to show the dimensions of the selection. In the width and height fields, enter the distance the stage has traveled in motor steps (ignore the um tag right now). Click Recalculate; a value should appear next to "um per pixel:" in the Calculated Results area.

## Rotational Axis

The bottom pane is the 'fun' part. Enter the current twister angle **in motor steps** (double-gradians; 0 is still 0, otherwise multiply the angle in degrees by 100/180 (5/9).). Enter a reasonable interval for delta-theta -- larger values should be more accurate, but will be much more involved to calibrate for. Make sure you're at theta-zero. Enclose your convenient bead in a rectangular ROI, making certain to leave some room around the edges (this is so the gaussian fitter knows what value is 'background'). Make sure the bead is focused by scrolling in and out a step or two to find the most intense slice. Then click the first Pick Bead button. It should replace its text with the location of the bead. (You'll probably need to stretch the calibrator window quite a bit.)

Now that you have the first location of the bead, you have to follow it through two rotations. The easiest way to do this is to use the motor controls on the SPIM plugin; increment the angle slider by one, refocus on the bead, repeat until you've changed angles by delta-theta decided above. (You may wish to click Goto theta-one to make sure you are at the correct angle.) Repeat the process of picking the bead, clicking on the second Pick Bead button instead. Repeat all of this for the third and final bead location -- you've now enough information to determine the rotational axis.

## Final Steps

Once you have a pixel size and all three bead locations, you may need to click Recalculate. You should have 'reasonable' values for each calculated result: um per pixel is probably in the range of 0.4348 (varies depending on stage motors). A good rotational axis has minimal values for X and Z, and a value very close to 1 (or -1) for Y -- it's very near vertical. Rotational axis origin is difficult to prescribe a 'reasonable' value; the best I can suggest is that the X component shouldn't be far from your sample column.

After all of this, you may wish to click Save & Apply. The values will all be recorded; they'll be loaded the next time you click Calibrate -- the pixel size information should be fixed, but if you've touched the sample or holder at all, you should at minimum redetermine the rotational axis.

Now that you have these values, you should be able to get a multi-view rotation by holding Alt and moving the mouse back and forth over the live window. Be patient with it -- the positional motors aren't as quick as the twister, so they sometimes lag behind a bit. With a carefully calibrated system, the X and Y should remain fairly constant on the center of the image, though the system often becomes unfocused with longer rotations. If the direction of rotation seems wrong, you can try the Reverse Axis button on the calibrator.
