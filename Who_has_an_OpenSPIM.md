---
---
Feel free to edit this page with information about your system\! (If you
do not have an account yet, it is
[simple\!](http://openspim.org/Special:UserLogin?type=signup&returnto=Who+has+an+OpenSPIM%3F))

# Aachen, Germany

![OpenSPIM with temperature controlled sample chamber by Fraunhofer
IPT](IPT.png
"OpenSPIM with temperature controlled sample chamber by Fraunhofer IPT")

  - [Life Sciences Engineering Business
    Unit](http://www.ipt.fraunhofer.de/en/Businessunits/LifeSciencesEngineering.html)
    at the Fraunhofer Institute for Production Technology IPT.
  - Our OpenSPIM design has a temperature controlled sample chamber for
    long-term experiments and uses a timing belt for precise sample
    rotation.

  

# Dresden, Germany

![LOCI's L-SPIM, January 22, 2016](X-OpenSPIMs-Tomancak-Lab.jpg
"LOCI's L-SPIM, January 22, 2016")

  - X-OpenSPIMs for dual-sided illumination and dual-sided detection
  - 20x (Olympus) and 40x (Nikon) sample chambers
  - Andor sCMOS Neo cameras
  - 488/561 VersaLase
  - hardware-controlled laser triggering (Arduino)
  - operated by MicroManager

<!-- end list -->

  - [Tomancak
    group](http://www.mpi-cbg.de/research/research-groups/pavel-tomancak.html)
    at the Max-Planck Institute of molecular Cell Biology and Genetics.

  

# Madison, WI, USA

![LOCI's L-SPIM, January 22, 2016](LOCI-Setup.jpg
"LOCI's L-SPIM, January 22, 2016")

  - [The Laboratory of Optical and Computational Instrumentation
    (LOCI)](http://loci.wisc.edu/) run by [Kevin
    Eliceiri](http://loci.wisc.edu/people/kevin-eliceiri) at the
    University Wisconsin-Madison. It uses a Coherent Cube laser and a
    Hamamatsu Orca R^2 camera, being controlled by a 32-bit Windows XP
    computer.

<!-- end list -->

  - The OpenSPIM software was developed in this lab by Johannes
    Schindelin and Luke Stuyvenberg, and tested and refined with the
    help of Julie Last and Jayne Squirrel (see the
    [People](People "wikilink") page for details), using that setup. The
    source code is hosted on
    [GitHub](https://github.com/openspim/micromanager).

  

# Heidelberg, Germany

![COS Heidelberg OpenSPIM](COS_HD_OpenSPIM_1.JPG
"COS Heidelberg OpenSPIM")

  - [Maizel](http://www.cos.uni-heidelberg.de/index.php/a.maizel?l=_e)
    and [Lemke](http://www.cos.uni-heidelberg.de/index.php/s.lemke?l=_e)
    groups at the [Center for Organismal
    Studies](http://www.cos.uni-heidelberg.de/?l=_e) of the Heidelberg
    University.
  - This setup slightly differs from the specifications of OpenSPIM
    v1.0. In particular we use a [Cobolt
    laser](http://www.cobolt.se/mld488nm.html), Nikon lenses and an
    [Orca4](http://www.hamamatsucameras.com/flash4/l), the whole running
    under Windows7 Pro.
  - More details and pictures about the [COS Heidelberg
    OpenSPIM](COS_Heidelberg_OpenSPIM "wikilink").

  

# Cambridge, UK, Maths Department

![Fig. 1 Four-arm OpenSPIM](4arm_system.jpg "Fig. 1 Four-arm OpenSPIM")

  - The [Goldstein](http://www.damtp.cam.ac.uk/user/gold/?l=_e) group in
    the [Department of Applied Mathematics and Theoretical
    Physics](http://www.damtp.cam.ac.uk/?l=_e) at the University of
    Cambridge.

We recently extended to a 4-armed system (Fig. 1):

  - 4 port sample chamber:
    [Media:4\_port\_chamber.pdf](Media:4_port_chamber.pdf "wikilink")
  - dual sided illumination with Vortran VersaLase multiple wavelength
    laser module (488, 561, 647 nm).
  - dual sided detection with 2 Photometrics [Coolsnap
    Myo](http://www.photometrics.com/products/ccdcams/coolsnap-myo.php:l).
  - We included a Thorlabs
    [shutter](http://www.thorlabs.de/NewGroupPage9.cfm?ObjectGroup_ID=927?l)
    in the beam path.
  - For brightfield illumination during sample positioning we use a lamp
    that is temporarily inserted in one of the filter holders (Fig. 2):
    [Media:LED tube light.pdf](Media:LED_tube_light.pdf "wikilink")

As part of the Biomaker Challenge 2018 we added the following
modifications:

  - Adjustable metal feet were attached to the clamps that carry the
    detection arms to align the two cameras (Fig. 3)
  - We wanted to provide illumination for light dependent
    (photosynthetic) organisms between acquisitions of a time lapse
    recording.

For this we added a lamp that switches on when the laser shutter closes.
The LED driver is triggered by the laser shutter controller via a TTL
inverter (Fig. 4).

  - To improve the robustness of the sample positioning we designed 3D
    printable sample holders (Fig. 5).

See also [Dual-view imaging on
hackster.io](https://www.hackster.io/steph2/dual-view-imaging-in-a-custom-built-light-sheet-microscope-e4502f)

[File:20170621\_114544.jpg|300px|thumb|right|Fig](File:20170621_114544.jpg%7C300px%7Cthumb%7Cright%7CFig).
2 LED tube light for brightfield
[File:adjustable\_foot\_smaller.jpg|300px|thumb|right|Fig](File:adjustable_foot_smaller.jpg%7C300px%7Cthumb%7Cright%7CFig).
3 Adjustable foot to align detection arm
[File:Illumination.png|300px|thumb|right|Fig](File:Illumination.png%7C300px%7Cthumb%7Cright%7CFig).
4 Schematic for illumination between acquisitions
[File:sample\_holder.png|300px|thumb|right|Fig](File:sample_holder.png%7C300px%7Cthumb%7Cright%7CFig).
5 3D-printed sample holder

  

# Cambridge, UK, MRC LMB

  - The Light Microscopy Facility at the [Medical Research Council's
    Laboratory of Molecular
    Biology](http://www.http://www2.mrc-lmb.cam.ac.uk/)
  - Our system features two-sided excitation with adjustable focus of
    the sheet lenses (Olympus 5x/0.15 air MPLFLN5X) which sit outside
    the imaging chamber to cope with different refractive indices.
  - 4 laser lines - combined in a separate laser bed and fed into a
    fibre (405nm & 640nm: both Coherent Cube; 488nm & 561nm: both
    Coherent Sapphire)
  - The imaging chamber can be heated to e.g. 37C for live cell imaging
    purposes.
  - Imaging lens is a Nikon 16x/0.8NA (N16XLWD-PF) with 3mm WD.
  - In front of the camera is a Thorlabs 6-position filter wheel
    (FW102C)
  - The entire system is portable (sort of) and modified to be laser
    safe as it is operated within our multi-user facility.

  

# Melbourne, Australia

![OpenSPIM system using the Picard high-resolution stage and an Andor
Neo camera in the Petrou Lab, Melbourne, Australia.](Petrou_SPIM.jpg
"OpenSPIM system using the Picard high-resolution stage and an Andor Neo camera in the Petrou Lab, Melbourne, Australia.")

  - The Petrou group at the [Florey
    Institute](http://http://www.florey.edu.au/research/ion-channels-disease?l=_e)
    the [Centre for Neural
    Engineering](http://www.cfne.unimelb.edu.au/research-laboratories/neurobiology/?i=_e)
    and the [Centre for Integrated Brain
    Function](http://www.cibf.edu.au//?i=_e) at the University of
    Melbourne.
  - We are deploying OpenSPIM for CLARITY and Scaleview based imaging of
    brain tissue for studying neural morphology. We use Dragon Lasers
    and an Andor Neo sCMOS camera.
  - More pictures to come\!

  

# Berlin, Germany

![OpenSPIM at Humboldt University Berlin](OpenSPIM_Berlin_top_view.png
"OpenSPIM at Humboldt University Berlin")

  - The Scholtz group at the [Humboldt University
    Berlin](http://www2.hu-berlin.de/biologie/zoologie/carsten_wolff/carsten.html?l=_e).
  - I am interested in morphogenetic processes during early development
    of arthropods like the water flea Daphnia magna, the woodlouse
    Porcellio scaber or the beachhopper Parhyale hawaiensis. Using the
    SPIM technique for live imaging experiments enables us to observe
    dynamic and complex processes like gastrulation and beginning
    morphogenesis.
  - We implemented a Coherent Obis 561 nm laser and a Hamamatsu
    OrcaFlash4 sCMOS camera into the OpenSPIM system. The system runs at
    the moment with just one-side illumination. However, the sample
    chamber is already made for dual-side illumination (2x 10x
    illumination and 16x detection). Additionally we integrated a
    Nikon-module that allows us to increases our range of magnification
    (1x, 1,25x, 1,5x, 2x).
  - More pictures to come\!

  
![T-SPIM chamber, designed by Pete Pitrone and build at the workshop of
the MPI CBG Dresden. ](T-SPIM_chamber.png
"T-SPIM chamber, designed by Pete Pitrone and build at the workshop of the MPI CBG Dresden. ")

  

# Exeter, UK

![OpenSPIM at the University of Exeter.](OpenSPIM_System.jpg
"OpenSPIM at the University of Exeter.")

  - The [College of Life and Environmental
    Sciences](http://lifesciences.exeter.ac.uk/) in association with the
    [College of Engineering, Mathematics and Physical
    Sciences](http://emps.exeter.ac.uk/).
  - We have constructed the system with a Melles Griot 488nm Argon laser
    and a Zyla 5.5 sCMOS camera running on 64-bit Windows 7 to image
    transgenic zebrafish.
  - The system currently has magnification options of 0.5x and 1x and
    1-photon illumination with plans to upgrade to 2-photon in the
    future.
  - More pictures to come\!

  

# Oulu, Finland

![OpenSPIM at the University of Oulu.](OpenSPIM_Oulu_top_view.jpg
"OpenSPIM at the University of Oulu.")

  - The [Light Microscopy Core Facility, at the Biocenter Oulu and the
    University of Oulu](http://www.oulu.fi/biocenter/lm).
  - Modified T-SPIM: dual side illumination with Vortran Stradus 488nm
    and 561nm lasers, ScopeLed G180 for bright field/transmitted light
    imaging, Olympus UMPLFLN 20X/0.5 W and Olympus LUMPLFLN 40X/0.8 W
    detection objectives, Hamamatsu ORCA-Flash 4.0 V2 camera.
  - Temperature, CO2 and O2 controlled liquid exchange/perfusion system
    for live cell imaging.
  - OpenSPIM has been used for live cell imaging: different cell types
    and spheroids in different 3D culture matrices, e.g. in Matrigel,
    collagen, myogel and fibrin mounted inside FEP tubes, and also for
    imaging living mouse skin cancer biopsies. It has also been used for
    whole mount stained and/or transgenic (expressing tdTomato, GFP,
    mCherry…) fixed samples, typically mouse embryonic kidneys, pieces
    of adult mouse tissues like heart, liver, fat, lung etc.

  

# Indianapolis, IN, USA

![OpenSPIM at IUSM.](OpenSPIM_IUSM_LCDs.jpg "OpenSPIM at IUSM.") ![IU
OpenSPIM chamber with oblique
illumination.](OpenSPIM_IUSM_Chamber_illuminated.jpg
"IU OpenSPIM chamber with oblique illumination.")

  - The [Indiana Center for Biological Microscopy at Indiana University
    School of Medicine](http://web.medicine.iupui.edu/icbm/).
  - We extended the base L-SPIM design for use in a core facility by
    including additional excitation wavelengths and support for live
    imaging. We are imaging with an ORCA Flash 4.0 v2 using CameraLink.
  - To support more fluorophores we incorporated five laser lines (442,
    488, 514, 568 and 647 nm) with AOTF modulation controlled via an
    [Arduino](https://www.arduino.cc) based [6 channel
    DAC](http://www.ti.com/product/tlv5618a). Emission wavelength
    filtering is with a workhorse [Sutter
    Lambda 10-2](http://www.sutter.com/IMAGING/lambda102.html).
    Multichannel acquisition is fully controlled (AOTF, filter wheels,
    etc) by a custom version of the SPIM Acquisition Plugin and
    derivations of the Arduino device adapter for MicroManager. To
    assess laser power, a motorized mirror and ThorLabs detector have
    been incorporated prior to beam shaping.
  - To support live imaging we have incorporated a perfusion and
    temperature control system into the standard L-SPIM chamber(no
    drilling etc.) built with off-the-shelf components (shout-out to
    [Adafruit](http://www.adafruit.com) and
    [Sparkfun](http://www.sparkfun.com)). It is Arduino based and relies
    on a bunch of pumps and thermistors. MicroManager integration and a
    CO2 loop is in the works (anyone with experience implementing
    [amphenol CO2
    sensors](http://www.mouser.com/ProductDetail/Amphenol-Advanced-Sensors/T6615-50K/?qs=sGAEpiMZZMvhkhGuTKDegrl2ezYd2qTk)?).
  - Our OpenSPIM is fully contained to simplify laser safety. To
    facilitate alignment and sample positioning a secondary camera
    driven by a [RaspberryPi](https://www.raspberrypi.org) provides a
    live image of the chamber with oblique RGB LED illumination from an
    Arduino and PWM via the 16 channel
    [TLC5940](http://playground.arduino.cc/Learning/TLC5940).
  - To aid in sample positioning a knob bar is under development with
    four free-turning knobs-one for each axis with position feed-back.
  - IU OpenSPIM has been used for imaging of Zebrafish (live heart-beat
    and fixed and cleared tissue), organoids, and tissue samples
    including rat kidneys-most in FEP tubing. It has also been a testbed
    for new technologies and methodologies.

<!-- end list -->

  - Links to schematics, Arduino firmware, PCB designs, MicroManager
    device adapters coming soon\!

  

-----

# Whole-brain imaging based on OpenSPIM, Warsaw, Poland

![Cleared-tissue imaging SPIM at the Nencki
Institute.](WarsawSPIM_doubleIllum.jpg
"Cleared-tissue imaging SPIM at the Nencki Institute.")

  - We are the Laboratory of Neurobiology at the Nencki Institute of
    Experimental Biology, Warsaw, Poland
    [1](http://www.nencki.gov.pl/pracownia-neurobiologii)
  - Using OpenSPIM as the starting point, we developed a cleared-tissue
    imaging SPIM system using dry 4X/0.13 Nikon objectives with WD of 17
    mm, or about 25 mm in immersion
  - We use 3D printed chambers for CLARITY- and CUBIC-cleared tissue and
    glass cuvettes for BABB-cleared tissue
  - Recently we replaced the Picard stage with one by Standa, with
    greatly increased speed and travel range at comparable cost
  - Also recently a second illumination arm was added, converting the
    setup from the L to the T configuration
  - Ar-Ion laser (458/488/515 nm with manual filter wheel for wavelength
    selection) used for illumination
  - beam height is raised to 65 mm, mainly for compability with the
    argon laser
  - we have demonstrated whole mouse and rat brain imaging (see
    [paper](http://www.nature.com/articles/srep28209/))

  

# Newcastle (HMRI/UoN), Australia

![OpenSPIM HMRI/UoN glamour
shot](Cylindrical_lens_and_corner_mirror2.jpg
"OpenSPIM HMRI/UoN glamour shot")

  - The 3D Tissue Clearing and Lightsheet Microscopy Facility
    (HMRI/UoN).
  - Our focus is on the development and progression of 3D histology in
    medical and plant sciences.
  - Imaging is performed with an OpenSPIM-based T-SPIM with Hammamatsu
    Orca Flash, Arduino controlled 405, 473 and 532nm CNI lasers, and
    Thorlabs emission filters and dichroics
  - Picard 4D stage controlled by wireless 3D 'spacemouse' - highly
    recommended.
  - Controlled via Micromanager, with 3D dataprocessing performed with
    FIJI, Terastitcher and Vaa3D using the UoN HPC Cluster
  - Currently building a new SPIM incorporating a digitally scanned
    lightsheet (to take advantage of the lightsheet mode of the Orca
    Flash), two Nikon x4 Plan Fluorite illumination objectives (17mm
    WD), 1" optics, enlarged chamber, and a long working distance RI
    corrected detection objective for imaging large, cleared tissues

  

# London, UK

![OpenSPIM with two lasers (VersaLase: 488, 561) and dual sided
illumination running in the the Max Telford Lab (UCL,
UK)](OpenSPIM_Telford-Lab_UCL.png
"OpenSPIM with two lasers (VersaLase: 488, 561) and dual sided illumination running in the the Max Telford Lab (UCL, UK)")

  - OpenSPIM running at the Max Telford Lab, University College London
  - It builds on the standard design with the addition of two colour
    laser illumination (VersaLase™ Multiple Wavelength System) and dual
    sided illumination.
  - To reduce image acquisition time ESio’s TTL controller box was
    incorporated
  - The OpenSPIM is used for high resolution 3d images and time lapse
    recordings to study the development of different lophotrochozoan
    members (Spiralia) in particular the polyclad flatworm *Maritigrella
    crozieri*.
  - For detailed information of our system and our experience of
    building it you can read our paper: Light-sheet microscopy for
    everyone? Experience of building an OpenSPIM to study flatworm
    development (BMC Developmental Biology, 2016)
