---
---
<div cellspacing="5" style="width: 31em; font-size: 90%; text-align:left; float:right; position:relative; border:2px; border-style:solid;">

### News

* [2015-10-16 Brightfield illumination by Michael Redd](/2015-10-16_Brightfield_illumination_by_Michael_Redd)
* [2014-08-15 EMBO practical course on light sheet microscopy](/2014-08-15_EMBO_practical_course_on_light_sheet_microscopy)
* [2014-04-22 Multiview deconvolution](/2014-04-22_Multiview_deconvolution)
* [2014-04-11 Sample prep for Zebrafish embryo](/2014-04-11_Sample_prep_for_Zebrafish_embryo)
* [2013-12-15 OpenSPIM optics 101](/2013-12-15_OpenSPIM_optics_101)

</div>

## The Idea

OpenSPIM is an *Open Access* platform for applying and enhancing **Selective Plane Illumination Microscopy** (*SPIM*).

> We hope that OpenSPIM in its radical openness will demonstrate that the
> benefits brought to science by the Open Source approach apply equally well to
> hardware.

## SPIM principle

{% include figure src="SPIM_logo.jpg" alt="SPIM schematic" %}

The SPIM technology offers fast, optically-sectioning, minimally-invasive 3D acquisition of fluorescing specimen over time. It achieves that by focusing a thin laser light-sheet into the specimen, taking two-dimensional images of the illuminated slice with a perpendicularly positioned detector (CCD camera). Three-dimensional stacks are obtained by moving the specimen orthogonal to the light-sheet between consecutive images. By mounting the sample in a rigid medium, e.g. agarose, and hanging it into the sample chamber in front of the detection lens, it is possible to rotate the sample and collect 3d stacks from
multiple angles (views).

## OpenSPIM

{% include figure src="Combined_solidworks_real_registered_small_faster.gif" caption="OpenSPIM buildup" %}

OpenSPIM is a platform to build, adapt and enhance SPIM technology. It is designed to be as accessible as possible:

* [Detailed, easy-to-follow build instructions](Step_by_step_assembly)
* [Off-the-shelf components and 3D-printed parts](Table_of_parts)
* [Modular](images/Combined_OpenSPIM_buildup_looped.gif) and [extensible](Configurations) design
* Completely open blueprints
* Completely Open Source

The build instructions are intended to allow scientists without prior knowledge in building optical systems to make their own OpenSPIM set-up. If a 3D printer is not readily available, the parts are designed to be easily machined by any competent work shop. The set-up is small enough to fit inside a [suitcase](images/SPIM_in_a_suitcase.jpg). The software is built on top of the
Open Source projects [µManager](https://micro-manager.org/) and [Fiji](https://fiji.sc/).

OpenSPIM is designed to be maximally cost-effective allowing anyone to build an entry level system and further tweak it for the specific imaging needs. Parallel set-ups ([SPIM farms](images/2I_1D_OpenSPIM_farm_02.jpg)) can be realized to enable medium throughput, long-term, time-lapse imaging.

OpenSPIM aims to creates a powerful synergy between Open Software and Open Hardware that can serve as a nucleus for further development of the SPIM technology.

## SPIM application

{% include figure src="HisYFP_front_page.gif" title="OpenSPIM recording of Drosophila embryogenesis" width="200" caption="OpenSPIM recording of Drosophila embryogenesis" %}

SPIM promises to revolutionize several fields of biological research, in particular developmental and cell biology, by allowing imaging of large samples with high resolution over extended periods of time. SPIM has been used in a spectacular fashion to record the development of embryos of model organisms such as *Drosophila* and zebra fish with cellular resolution throughout the developing specimen (the so-called *in toto* imaging). The ability of SPIM to deliver high signal-to-noise 3D images of large specimen from different angles in an extended time-lapse is currently hard to achieve with any other microscopy technology. Since monitoring biological systems with high resolution over time is the goal of essentially all fields of biological inquiry, SPIM technology is imminently useful to biologists.

## Partners and funding

<img src="images/Mpi-cbg-logo.gif" width="150" alt="Mpi-cbg-logo.gif"/> <img src="images/LOCI_logo.jpg" width="150" alt="LOCI_logo.jpg"/> <img src="images/LMF_logo.jpg" width="80" alt="LMF_logo.jpg"/> <img src="images/ERC_acronym.jpg" width="100" alt="ERC_acronym.jpg"/> <img src="images/RMS_logo.jpg" width="150" alt="RMS_logo.jpg"/>

# Building your own OpenSPIM

  - [Table of Parts](Table_of_parts)
  - [Step by step assembly](Step_by_step_assembly)
  - [How to install](How_to_install) the Micro-Manager
    software with SPIM support.
  - [How to operate](Operation) OpenSPIM including sample
    preparation, calibration and data processing.

Please feel free to put information about your system on <a href="Who_has_an_OpenSPIM">this page</a>!

# OpenSPIM data

Check the <a href="Gallery#OpenSPIM_data">gallery</a> to see more!

## MAMED EMBO course

{% include gallery-begin %}
{% include gallery-video id="Jusr_J15FXU" width="400" height="243" caption="Marine annelid *Platynereis dumerilii* stained with Sytox-green imaged with OpenSPIM from 7 angles. Walk through fused and deconvolved data (15 iterations on default settings). Staining, OpenSPIM assembly and imaging done by Mette Handberg-Thorsager, processing by Pavel Tomancak. " %}
{% include gallery-end %}


## Fruit fly

{% include gallery-begin %}
{% include gallery-video id="kZKHuKscKcQ" width="400" height="243" caption="Histone-YFP from gastrulation to beginning of muscle contraction from ventral, lateral and dorsal view
" %}
{% include gallery-video id="bdT1XK-0jCM" width="400" height="243" caption="Expression pattern of Csp-sGFP recorded with OpenSPIM" %}
{% include gallery-end %}

## Zebrafish

{% include gallery-begin %}
{% include gallery-image src="Zebrafish_fused_max_gamma0.8.png" width="400" caption="Multi-position z-stack of a living 48 hpf Tg(Bactin:H2A-EGFP) zebrafish, stitched using the Grid/Collection Plugin in Fiji. Maximum intensity projection, gamma 0.8. " %}
{% include gallery-video id="kZKHuKscKcQ" width="400" height="243" caption="Beating heart of a 48 hpf Tg(cmlc2:EGFP) zebrafish. Left: overlay of transmitted light and fluorescence signal. Right: fluorescence signal. " %}
{% include gallery-end %}

## Twitter

Follow OpenSPIM on Twitter for news on light sheet microscopy: <a href="https://twitter.com/openspim">@OpenSPIM</a>
