---
---
Now that we have assembled the OpenSPIM microscope it is time to start
using it. We will need to prepare a sample, align the light sheet
(Calibration), set-up the acquisition and process the data.

# Sample Preparation

![Pulling Drosophila embryos in agarose inside a glass capilary (*with
some priceless random audio*)](Pulling_embryos_into_capillary.ogv
"Pulling Drosophila embryos in agarose inside a glass capilary (with some priceless random audio)")
The basic principles of sample preparation for SPIM differs from
traditional microscopy technologies. There are no glass slides or
coverslips. Instead, the sample needs to be suspended in a water filled
chamber in front of the lens so that it can be rotated. This is usually
achieved by embedding the sample in a low melting point (LMP) agarose
inside a glass capillary equipped with a plunger. For imaging, the
agarose column with the specimen is pushed out of the capillary using
the plunger to hang in front of the lens.

For the purpose of making registration easier, we mix the sub-resolution
fluorescent beads into the specimen containing agarose slurry and use
them as fiduciary markers to align the different SPIM views. The
software to do that is available in [Fiji](http://fiji.sc).

Follow the link to check our resources for [**sample
preparation**](Sample_Preparation "wikilink").

# Calibration

![OpenSPIM rendering with laser on](1I_1D_OpenSPIM.png
"OpenSPIM rendering with laser on") Before using the OpenSPIM the light
sheet needs to be [**aligned**](Light-sheet_Calibration "wikilink").
This means that the light sheet needs to be shaped by the optics of the
system to be parallel to the imaging plane of the camera, perpendicular
to the detection axis, as thin as possible, uniform across the field of
view and, most importantly, in focus with the detection objective. Since
the procedure is rather involved, we provide a series of detailed videos
that illustrate the process. Innovations are welcome.

Although the light sheet is rather stable once aligned, it should be
[**aligned**](Light-sheet_Calibration "wikilink") at regular intervals
or whenever the image quality or point spread function (PSF) of the
beads looks suboptimal.

We also recommend examining the signal in the imaged specimen and
tweaking the light sheet using the bottom knob on the lower left corner
mirror of the set-up to optimize the image quality. The knob moves the
light sheet roughly parallel to the focal plane of the detection lens,
and thus moving it back and forth focuses the lens into the middle of
the light sheet.

  - **[gel for beadscans and Matlab script to evaluate
    them](http://www.dkfz.de/Macromol/quickfit/beadscan.html)**. Using
    this you can estimate the size of the PSF of your microscope

It is also possible to measure the [light-sheet
thickness](Light_sheet_characterization "wikilink") using a small mirror
mounted in the sample chamber.

# Software

![Screenshot of OpenSPIM stage control](Stagecontrols.png
"Screenshot of OpenSPIM stage control")

OpenSPIM relies on [µManager](http://valelab.ucsf.edu/~MM/MMwiki/) run
under [Fiji](http://fiji.sc). Make sure you [**download and
install**](Downloads "wikilink") all the required components.

Next, please follow the instructions to [**configure the
hardware**](Downloads#Initial_hardware_configuration "wikilink")
properly before trying to acquire images.

[**Start up**](OpenSPIM_Software_start_up "wikilink") the OpenSPIM
µManager plugin.

Make yourself familiar with the operation of the OpenSPIM [**stage
control**](OpenSPIM_stage_control "wikilink").

Now you are ready to [**acquire**](Acquisition "wikilink") images.
Please follow these step-by-step tutorials:

  - [Acquiring a Single
    Image](Acquisition#Acquiring_a_Single_Image "wikilink")
  - [Acquiring a Stack](Acquisition#Acquiring_a_Stack "wikilink")
  - [Single-Plane Time
    Lapse](Acquisition#Single-Plane_Time_Lapse "wikilink")
  - [Multi-View Imaging of a Fixed
    Sample](Acquisition#Multi-View_Imaging_of_a_Fixed_Sample "wikilink")
  - [Multi-View Time Lapse imaging of Live
    Sample](Acquisition#Multi-View_Time_Lapses "wikilink")

# Data processing

The raw multi-view OpenSPIM data need to be processed in order to
achieve *in toto* imaging of large biological sample. We describe here
the steps of the SPIMage processing pipeline as implemented in Fiji. The
processing involves saving the data in a format accessible by Fiji's
SPIM registration plugins, registration of the views using beads as
fiduciary markers, fusion of the data from different views into a single
output image (potentially by employing multi-view deconvolution),
stabilisation of the time-lapse data by registration across time-points
using the segmented beads, exploration of the raw and fused data in
space and time and finally 3D rendering for presentation purposes.

  - [**System requirements**](Pre-requisites "wikilink") for SPIMage
    processing

<!-- end list -->

  - ['''Download sample data](Raw_data "wikilink") from Dresden's
    OpenSPIM.

<!-- end list -->

  - [**Pre-processing**](Pre-processing "wikilink") of OpenSPIM ome.tiff
    stacks for multi-view reconstruction.

<!-- end list -->

  - [**Registration**](Registration "wikilink") of multi-view OpenSPIM
    acquisition using bead based registration plugin in Fiji.

<!-- end list -->

  - [**Fusion**](Fusion "wikilink") of registered multi-view OpenSPIM
    data into s a single output image using content based fusion or
    multi-view deconvolution.

<!-- end list -->

  - [**Time lapse registration**](Timelapse_Registration "wikilink") of
    long-term time lapse data.

<!-- end list -->

  - [**Browsing**](Browsing "wikilink") of OpenSPIM data with Fiji's
    BigDataViewer (coming soon).

<!-- end list -->

  - [**3D rendering**](3D_rendering "wikilink") of fused OpenSPIM data.

If you have a cluster available, you could imitate the way the Tomancak
group executes [SPIM Registration on their
cluster](http://fiji.sc/SPIM_Registration_on_cluster).

[Category:Hardware](Category:Hardware "wikilink")
[Category:Operation](Category:Operation "wikilink")
[Category:Software](Category:Software "wikilink")
