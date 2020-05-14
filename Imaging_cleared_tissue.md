This page concerns optical tissue clearing (that is, rendering it
transparent in order to image deeper) and imaging in a setup based on
OpenSPIM.

# Tissue clearing

There now exist a range of tissue clearing techniques for both mammalian
and plant tissues. From imaging point of view, they fall into two
categories:

  - solvent-based methods (BABB, ...DISCO) result in refractive index in
    the 1.55-1.56 range. These methods usually lead to sample shrinkage.
    The solvents are incompatible with most objectives and materials.
  - hydrogel and other aqueous methods (CLARITY, Scale, CUBIC etc. )
    yield samples with refractive index 1.47-1.49. Samples often swell.
    Ordinary immersion objectives can be used.

## Online resources for tissue clearing protocols

  - For a summary of various clearing techniques, and detailed
    instructions for performing CLARITY (excellent for neural tissue),
    please consult the following manual compiled by the 3D Tissue
    Clearing and Lightsheet Microscopy Facility (HMRI/UoN)
    [Media:3D\_Tissue\_Clearing\_Handbook\_3rd\_Ed.pdf](Media:3D_Tissue_Clearing_Handbook_3rd_Ed.pdf "wikilink")

<!-- end list -->

  - [CLARITY resource center](http://clarityresourcecenter.org/)

<!-- end list -->

  - [iDISCO method](https://idisco.info/)

# Immersion media

Generally cleared tissue has a higher refractive index than water. To
prevent losing focus when moving the sample, you have to use immersion
medium with the same RI as the sample.

Most protocols recommend using the same reagent for RI matching and for
imaging. This has some disadvantages - some reagents are too expensive
to fill the entire light-sheet microscope chamber, others sometimes
crystallize, react with outside air etc. Cheap and user-friendly
alternatives for imaging include

  - glycerol in the right concentration (80% has been used for CLARITY
    by [Epp et al.](http://eneuro.org/content/2/3/ENEURO.0022-15.2015))
  - microscopy immersion oil
  - the authors of [CUBIC
    paper](http://www.sciencedirect.com/science/article/pii/S0092867414004188)
    recommend a a 1:1 mixture of silicon oil TSF4300 (Momentive
    Performance Materials, RI = 1.498) and mineral oil (Sigma-Aldrich,
    RI = 1.467).

# Objectives & chambers

Optimally, an immersion objective matched to the tissue refractive index
should be used. Such objectives exist (by Zeiss, Olympus and Leica at
the time of writing), but are very expensive. Long working distance air
and water objectives can be used as well, but their performance will be
somewhat limited by aberrations. Keep in mind that working distance
changes if the immersion medium RI changes - this has to be taken into
account when designing the setup.

# Sample mounting

For confocal or two-photon microscopy, a chamber with depth equal to the
sample thickness should be be used. For designs see: [CLARITYT
Wiki](http://wiki.claritytechniques.org/index.php/Sample_Mounting#Whole_brain_mounting_for_confocal_imaging),
[iDISCO
protocol](https://idiscodotinfo.files.wordpress.com/2015/03/idisco-whole-mount-staining-bench-protocol-may-2016.pdf),
[HMRI/UoN
handbook](http://openspim.org/images/a/a8/3D_Tissue_Clearing_Handbook_3rd_Ed.pdf)

For SPIM, the sample had to be suspended in a chamber filled with
immersion medium. One way to do it is glue the sample to a glass slide
mounted in a holder that in turn is mounted in the SPIM setup in place
of the capillary. To glue a cleared sample, first pat with lint-free
tissue. Cyanoacrylic glues (like Superglue) tend to work - sometimes it
helps to try two or three brands, they differ in composition.

![Glass slide holder used in the SPIM for brains setup
[1](http://www.nature.com/articles/srep28209). This holder can be
mounted on the stage arm using a M6 screw. Glass slide can be mounted
with a M3 nylon or nylon-tipped screw. ](Holder.PNG
"Glass slide holder used in the SPIM for brains setup 1. This holder can be mounted on the stage arm using a M6 screw. Glass slide can be mounted with a M3 nylon or nylon-tipped screw. ")
