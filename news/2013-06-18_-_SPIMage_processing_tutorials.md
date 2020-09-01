---
---
Integral part of SPIM imaging is data processing sometimes referred to as **SPIMage processing**. The OpenSPIM project relies on tight integration with [Fiji](https://fiji.sc) where most of the algorithms for SPIMage processing have been implemented in the past.

We have assembled [**extensive tutorials**](Operation#Data_processing) that will walk you through all the steps required to put multi-view SPIM data together.

  - We start by defining [**System requirements**](Pre-requisites) and downloading [sample OpenSPIM data](Raw_data), - followed by optional [**pre-processing steps**](Pre-processing).
  - [**Multi-view registration**](Registration) is at the heart of SPIMage processing pipeline.
  - [**Multi-view Fusion**](Fusion) section discusses how to combine several view into one output image
  - [**Time series registration**](Timelapse_Registration) removes the sample drift across long-term timelapse.

The pipeline is relatively linear as described above, we highlight the steps where [**alternative routes exist**](Registration#cross-road_in_spim_plugins).

Theoretical principles of the methods involved are best described on the [SPIM pages of Fiji wiki](https://fiji.sc/SPIM_Registration).

The description of several steps of the SPIMage processing pipeline are still in the works. Particularly [**multi-view deconvolution**](Fusion#deconvolution), [**data viewing**](https://fiji.sc/BigDataViewer) and [**3D rendering**](3D_rendering). Stay tuned.
