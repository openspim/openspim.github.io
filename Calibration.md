---
title: Calibration
layout: page
description: Light-sheet calibration (alignment)
---

{% include image src="1I_1D_OpenSPIM.png" width="70%" caption="OpenSPIM rendering with laser on" %}

Before using the OpenSPIM the light sheet needs to be [**aligned**](Light-sheet_Calibration).
This means that the light sheet needs to be shaped by the optics of the system to be parallel to the imaging plane of the camera, perpendicular to the detection axis, as thin as possible, uniform across the field of view and, most importantly, in focus with the detection objective. Since the procedure is rather involved, we provide a series of detailed videos that illustrate the process. Innovations are welcome.

Although the light sheet is rather stable once aligned, it should be [**aligned**](Light-sheet_Calibration) at regular intervals or whenever the image quality or point spread function (PSF) of the beads looks suboptimal.

We also recommend examining the signal in the imaged specimen and tweaking the light sheet using the bottom knob on the lower left corner mirror of the set-up to optimize the image quality. The knob moves the light sheet roughly parallel to the focal plane of the detection lens, and thus moving it back and forth focuses the lens into the middle of the light sheet.

  - **gel for bead scans and Matlab script to evaluate them**. Using this you can estimate the size of the PSF of your microscope

It is also possible to measure the [light-sheet thickness](Light_sheet_characterization) using a small mirror mounted in the sample chamber.