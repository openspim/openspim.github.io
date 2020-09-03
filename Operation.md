---
title: Microscope Operation
layout: page
description: Operating the OpenSPIM microscope
---
Now that we have assembled the OpenSPIM microscope it is time to start using it. We will need to prepare a sample, align the light sheet (Calibration), set-up the acquisition and process the data.

# Sample Preparation

{% include video id="G6P52G06oPw" width="400" height="243" caption="Pulling Drosophila embryos in agarose inside a glass capillary (*with some priceless random audio*)" %}

The basic principles of sample preparation for SPIM differs from traditional microscopy technologies. There are no glass slides or coverslips. Instead, the sample needs to be suspended in a water filled chamber in front of the lens so that it can be rotated. This is usually achieved by embedding the sample in a low melting point (LMP) agarose inside a glass capillary equipped with a plunger. For imaging, the agarose column with the specimen is pushed out of the capillary using the plunger to hang in front of the lens.

For the purpose of making registration easier, we mix the sub-resolution fluorescent beads into the specimen containing agarose slurry and use them as fiduciary markers to align the different SPIM views. The software to do that is available in [Fiji](https://fiji.sc).

Follow the link to check our resources for [**sample preparation**](Sample_Preparation).

# Calibration

{% include image src="1I_1D_OpenSPIM.png" width="70%" caption="OpenSPIM rendering with laser on" %}

Before using the OpenSPIM the light sheet needs to be [**aligned**](Light-sheet_Calibration).
This means that the light sheet needs to be shaped by the optics of the system to be parallel to the imaging plane of the camera, perpendicular to the detection axis, as thin as possible, uniform across the field of view and, most importantly, in focus with the detection objective. Since the procedure is rather involved, we provide a series of detailed videos that illustrate the process. Innovations are welcome.

Although the light sheet is rather stable once aligned, it should be [**aligned**](Light-sheet_Calibration) at regular intervals or whenever the image quality or point spread function (PSF) of the beads looks suboptimal.

We also recommend examining the signal in the imaged specimen and tweaking the light sheet using the bottom knob on the lower left corner mirror of the set-up to optimize the image quality. The knob moves the light sheet roughly parallel to the focal plane of the detection lens, and thus moving it back and forth focuses the lens into the middle of the light sheet.

  - **gel for bead scans and Matlab script to evaluate them**. Using this you can estimate the size of the PSF of your microscope

It is also possible to measure the [light-sheet thickness](Light_sheet_characterization) using a small mirror mounted in the sample chamber.

# Software

{% include image src="Stagecontrols.png" width="70%" caption="Screenshot of OpenSPIM stage control" %}

OpenSPIM relies on [µManager](https://micro-manager.org/wiki/) run under [Fiji](https://fiji.sc). Make sure you [**download and install**](Downloads) all the required components.

Next, please follow the instructions to [**configure the hardware**](Downloads#Initial_hardware_configuration) properly before trying to acquire images.

[**Start up**](OpenSPIM_Software_start_up) the OpenSPIM µManager plugin.

Make yourself familiar with the operation of the OpenSPIM [**stage control**](OpenSPIM_stage_control).

Now you are ready to [**acquire**](Acquisition) images. Please follow these step-by-step tutorials:

  - [Acquiring a Single Image](Acquisition#Acquiring_a_Single_Image)
  - [Acquiring a Stack](Acquisition#Acquiring_a_Stack)
  - [Single-Plane Time Lapse](Acquisition#Single-Plane_Time_Lapse)
  - [Multi-View Imaging of a Fixed Sample](Acquisition#multi_view_imaging_of_a_fixed_sample)
  - [Multi-View Time Lapse imaging of Live Sample](Acquisition#Multi-View_Time_Lapses)

# Data processing

The raw multi-view OpenSPIM data need to be processed in order to achieve *in toto* imaging of large biological sample. We describe here the steps of the SPIMage processing pipeline as implemented in Fiji. The processing involves saving the data in a format accessible by Fiji's SPIM registration plugins, registration of the views using beads as fiduciary markers, fusion of the data from different views into a single output image (potentially by employing multi-view deconvolution), stabilization of the time-lapse data by registration across time-points using the segmented beads, exploration of the raw and fused data in space and time and finally 3D rendering for presentation purposes.

  - [**System requirements**](Pre-requisites) for SPIMage processing
  - [**Download sample data**](Raw_data) from Dresden's OpenSPIM.
  - [**Pre-processing**](Pre-processing) of OpenSPIM ome.tiff stacks for multi-view reconstruction.
  - [**Registration**](Registration) of multi-view OpenSPIM acquisition using bead based registration plugin in Fiji.
  - [**Fusion**](Fusion) of registered multi-view OpenSPIM data into s a single output image using content based fusion or multi-view deconvolution.
  - [**Time lapse registration**](Timelapse_Registration) of long-term time lapse data.
  - [**Browsing**](https://fiji.sc/BigDataViewer) of OpenSPIM data with Fiji's BigDataViewer (coming soon).
  - **3D rendering** of fused OpenSPIM data (TBD).

If you have a cluster available, you could imitate the way the Tomancak group executes [SPIM Registration on their cluster](https://fiji.sc/SPIM_Registration_on_cluster).
