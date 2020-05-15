---
---
# Bright-field illumination

Michael Redd from the Cell Imaging Core Facility at the University of
Utah put together an Arduino-based solution to get proper bright-field
illumination in an OpenSPIM setup:
[Brightfield](Brightfield "wikilink").

# Shutter

Instructions to make an Arduino-controlled shutter compatible with
uManager: [paper by Todd P.
Meyrath](http://george.ph.utexas.edu/~meyrath/informal/shutter.pdf) and
[tutorial on the uManager
page](https://micro-manager.org/wiki/Control_laser_shutters_with_Arduino).

# Stepper Motor Upgrade

If you would like to swap out one of the Picard stepper motors you can
do so with a bit of effort.

Instructions about how to go about this for a Thorlabs DRV001 connected
via a Thorlabs BSC201 controller on a 64bit OpenSPIM setup are detailed
below (by Jerome Boulanger and Ben Sutcliffe):

1.  Download the micro-manager source code as instructed here
    (https://micro-manager.org/wiki/Micro-Manager\_Source\_Code).
2.  Instal all the relevant programs for building micro-manager as
    instructed here
    (https://micro-manager.org/wiki/Building\_MM\_on\_Windows).
3.  Setup up Visual C++ 2010 Express as here
    (https://micro-manager.org/wiki/Visual\_Studio\_project\_settings\_for\_device\_adapters).
4.  Instal the 64bit APT software from Thorlabs
    (https://www.thorlabs.com/software\_pages/ViewSoftwarePage.cfm?Code=Motion\_Control\&viewtab=1).
5.  Download and unzip the APTx64 form here
    (https://micro-manager.org/wiki/File:APT\_x64.zip).
6.  Then build the ThorlabsAPTStage Device Adapter in 64bit on a 64bit
    Windows 7 machine, using the 'APT.lib' downloaded in point 5.
7.  Rename the resulting .dll file to 'mmgr\_dal\_ThorlabAPTStage.dll'
    then place it into the OpenSPIM.app folder along with the 'APT.dll'
    downloaded in point 5.
8.  The OpenSPIM Fiji/MM bundle can then restarted and a ThorlabAPTStage
    could be configured as described for a 32bit system here
    (https://micro-manager.org/wiki/ThorlabsAPTStage).

More details to follow about incorporating this into the SPIMAcquisition
plugin.

# OpenSPIM for large samples

## Field of view

The original OpenSPIM uses a 2X expander to enlarge the laser beam to 2
mm. For larger samples a larger field of view can be preferable. This
means that you will need a larger beam to create a taller light sheet.
Change the second beam expander lens to f=75 mm or 100 mm and increase
the distance between lenses accordingly.

## Objectives

Immersion objectives with long working distance are hard to find.
However, at low NA and moderate magnification, a dry objective will also
work; the higher NA, the more spherical aberrations will be present.
Keep in mind that when using a dry objective in immersion, the WD will
increase (approximately by a factor equal to the RI of the new medium,
eg. 17 mm in air will increase to 22.6 mm in water).

## Example parts list

The table below lists the parts used by the OpenSPIM for brains setup
built by Monika Pawłowska (Nencki Institute of Experimental Biology,
Warsaw).

| Manufacturer | Accessibility | Description                                                                                                                                                                                                                 | File or Link/Model \#                                                                                                                                                                                                                                                              | Image                                                                     | Quantity                         | Price (EUR) |
| ------------ | ------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------- | -------------------------------- | ----------- |
| Nikon        | purchase      | 4X Nikon Plan Fluorite Imaging Objective, 0.13 NA, 17.2 mm WD, dry                                                                                                                                                          | [N4X-PF](https://www.thorlabs.de/thorproduct.cfm?partnumber=N4X-PF)                                                                                                                                                                                                                | [thumb|upright=0.7|center](File:Thorlabs_N4X-PF_objective.jpg "wikilink") | 2 (or 3 for double illumination) | 410         |
| Thorlabs     | purchase      | Translating Lens Mount for Ø1" Optics (for the objectives                                                                                                                                                                   | [LM1XY/M](https://www.thorlabs.de/thorproduct.cfm?partnumber=LM1XY/M)                                                                                                                                                                                                              | [thumb|upright=0.7|center](File:Thorlabs_LM1XY_mount.jpg "wikilink")      | 2 (or 3)                         | 125         |
| Nikon        | purchase      | Infinity-Corrected Tube Lens for Plan Fluorite Objectives                                                                                                                                                                   | [ITL200](https://www.thorlabs.de/thorproduct.cfm?partnumber=ITL200)                                                                                                                                                                                                                | [thumb|upright=0.7|center](File:Thorlabs_ITL200_lens.jpg "wikilink")      | 1                                | 405         |
| Monika       | self made     | This chamber can be 3D printed. For windows use 24x24 mm microscopy cover glasses and glue (eg. two component epoxy)                                                                                                        | [.stl on Github](https://github.com/openspim/openspim-parts/blob/master/Chambers/Dry_Objectives_Chamber_and_Holder/Chamber.stl)                                                                                                                                                    | [thumb|upright=0.7|center](File:Large_samples_chamber_3D.PNG "wikilink")  | 1                                |             |
| Monika       | self made     | This holder includes two threaded holes so it's easiest to make from metal (eg aluminum). Holder is mounted on the 4D stage arm with M6 screw. Glass slide with 1 mm thickness can be held with nylon or nylon-tipped screw | [drawing on Github](https://github.com/openspim/openspim-parts/blob/master/Chambers/Dry_Objectives_Chamber_and_Holder/Metal_Holder.pdf) [step file on Github](https://github.com/openspim/openspim-parts/blob/master/Chambers/Dry_Objectives_Chamber_and_Holder/Metal_Holder.step) | [thumb|upright=0.4|center](File:holder.PNG "wikilink")                    | 1                                |             |
