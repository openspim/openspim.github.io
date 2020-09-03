---
title: Anti-Drift
layout: page
description: Strategy to keep the entirety of the sample in the stack volume
---
Anti-drift is the process of ensuring that the target of imaging remains within the field of view of the camera. Because the sample is prone to drift -- most commonly due to the agarose shrinking, but sometimes due to the sample itself moving within the column or other factors entirely -- a strategy to keep the entirety of the sample in the stack volume must be implemented.

Please note that the OpenSPIM plugin's anti-drift requires a [calibrated pixel size](Pixel_Size_Calibration) to function properly. Uncalibrated systems will encounter severe troubles while applying the anti-drift corrections.

# Operation

The OpenSPIM plugin implements an interactive anti-drift strategy that combines phase correlation with manual correction to ensure the sample remains in view.

## Automatic Processing

As each stack is acquired, its slices are averaged together in three dimensions to yield three average-projections: XY, XZ, and ZY. Before the anti-drift GUI is displayed to the user, each of these projections is phase-correlated to the projection saved from the last time this same view was processed. Then the determined offset is applied and the GUI is displayed until the next time this view is to be imaged (or until the user dismisses it).

## Interactive Control

At this point, the user can make whatever changes they like:

  - The up, down, left, and right arrow keys shift the green image in the X/Y plane.
  - Page Up/Page Down move the green image in Z.
  - Holding shift will make these steps larger.
  - Press Enter to accept the correction, or Escape to make no correction at all.

If the current view starts to be acquired again (because the other views have all been acquired in the background and the next timepoint has begun), the offset will automatically be accepted as though the user had pressed Enter.

The goal of the interactive control is to align the green image with the crosshairs (representing the center of the stack to be acquired) in such a way that the entirety of the sample's image in green is within the borders of each projection. This will make sure the motors are positioned correctly the next time the stack is acquired.
