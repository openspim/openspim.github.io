---
title: Pixel Size Calibration
layout: page
description: Pixel size calibration
---
As a central feature for virtually all imaging, specifying a pixel's physical dimensions is handled within µManager:

## Determining the Pixel Size

### Using the Pixel Size Calibrator Tool

The SPIM Acquisition plugin comes with a pixel size calibration tool, accessed through the stage controls tab of the GUI. It is designed for use with a microscope calibration slide/fragment or similar well-defined structure. When you open it, it will make a copy of the current live view image as a new window. There are two options for determining the pixel size:

#### 1. Ruler Mode

If the only known physical distance is between two largely arbitrary points on the view, use ruler mode.

1.  Enter the physical distance in the "Length (um):" box.
2.  While Ruler Mode is selected, use ImageJ's line ROI tool (it should already be selected) to drag a line between the two points.
3.  The distance will be calculated and the pixel size derived.

#### 2. Grid Mode

If using a known microscope calibration grid or similar object, grid mode can be used. Grid mode attempts to fit a step model to the grid lines, to determine their center mathematically.

1.  Enter the physical distance between grid lines in the "Length (um):" box.
2.  Select the appropriate image type. If you have the grid at 45 degrees with respect to the camera, the distance must be multiplied by the square root of two to account for the angle.
    1.  If you are using transmission light, the grid will probably be dark (a shadow). Invert the image using Edit -> Invert to make the grid lines white.
3.  With Grid Mode selected, use ImageJ's line ROI tool to drag a line from one grid line to an adjacent, parallel grid line.
4.  The plugin will attempt to fit the grid lines, calculate the distance between them, and use that information to calculate the pixel size. Additionally, it will draw markers on what it believes to be the grid lines. If these are pointing incorrectly or are significantly far from the selected grid lines, the results may be incorrect.

When the correct pixel size has been determined (for OpenSPIM 1.0, this is approximately 0.652 µm/pixel), click Apply to create the pixel size definition. Note: You may need to go into µManager's pixel size calibration window, as described below, and delete the "Uncalibrated" entry. You should then save your hardware configuration (as this is where µManager stores the pixel size calibration): On the µManager window, click Tools -> Save Configuration Settings as... and browse to
and overwrite your configuration file.

### Manually Determining Pixel Size

#### Calculating the Pixel Size

{% include image src="Pixel-size-calibration-1.png" width="100%" caption="Determining motor step size in pixels" %}

{% include image src="Pixel-size-calibration-2.png" width="100%" caption="Determining motor step size in pixels" %}

The pixel size can also be determined manually from a less orderly sample:

1.  Load a sample into the system. Beads may be easiest, though anything with well-defined features will do.
2.  Using the motor navigation in µManager's Live Window, locate any such feature.
3.  Using Fiji's magnification tool, zoom in to allow for precise placement of a ROI.
4.  Using the line ROI tool, drag a line from a recognizable point on the feature to the right of it (the line's precise endpoint will be moved momentarily).
5.  On the OpenSPIM GUI, read the value of the X motor, then press the left arrow key. This will instruct µManager to move the stage by 10 µm. The actual distance may be not be 10 µm, so you should read the new value of the X motor and record the difference as X µm.
6.  While moving the endpoint of the line ROI to the new location of the feature, pay attention to Fiji's status bar: it displays the current length of the line.
7.  Once the line is spanning the distance the feature moved, record this distance as Y pixels.
8.  The value to use for your pixel size will be (X µm) / (Y pixels).

#### Updating µManager's Configuration

{% include image src="Pixel-size-calibration-3.png" width="100%" caption="Entering the pixel step size" %}

Now we'll enter the value into µManager's configuration. Click *Tools>Pixel Size calibration*

1.  The OpenSPIM plugin will have automatically provided a 'calibration' called (descriptively) "Uncalibrated" which sets a pixel to be 1 µm. This is to ensure that µManager's built-in Live Window panning (which requires an active pixel size calibration) works with minimal configuration. Select it, then click Edit.
2.  Re-labelling the configuration will help identify it, but isn't required.
3.  In the window that appears, replace the Pixel Size value (1.0) with the number calculated above.
4.  Click OK.
5.  Finally, click *Tools>Save configuration settings as...* and overwrite the current configuration file.
