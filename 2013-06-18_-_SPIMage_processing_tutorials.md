---
---
Integral part of SPIM imaging is data processing sometimes referred to
as **SPIMage processing**. The OpenSPIM project relies on tight
integration with [Fiji](http://fiji.sc) where most of the algorithms for
SPIMage processing have been implemented in the past.

We have assembled [**extensive
tutorials**](Operation#Data_processing "wikilink") that will walk you
through all the steps required to put multi-view SPIM data together.

  - We start by defining [**System
    requirements**](Pre-requisites "wikilink") and downloading
    ['''sample OpenSPIM data](Raw_data "wikilink"),
  - followed by optional [**pre-processing
    steps**](Pre-processing "wikilink").
  - [**Multi-view registration**](Registration "wikilink") is at the
    heart of SPIMage processing pipeline.
  - [**Multi-view Fusion**](Fusion "wikilink") section discusses how to
    combine several view into one output image
  - [**Time series registration**](Timelapse_Registration "wikilink")
    removes the sample drift across long-term timelapse.

The pipeline is relatively linear as described above, we highlight the
steps where [**alternative routes
exist**](Registration#Cross-road_in_SPIM_plugins "wikilink").

Theoretical principles of the methods involved are best described on the
[SPIM pages of Fiji wiki](http://fiji.sc/SPIM_Registration).

The description of several steps of the SPIMage processing pipeline are
still in the works. Particularly [**multi-view
deconvolution**](Fusion#Deconvolution "wikilink"), [**data
viewing**](Browsing "wikilink") and [**3D
rendering**](3D_rendering "wikilink"). Stay tuned.

[Category:News](Category:News "wikilink")
