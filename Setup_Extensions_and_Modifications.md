---
title: Setup Extensions and Modifications
layout: page
description: Additional setup tweaks
---
# Bright-field illumination

Michael Redd from the Cell Imaging Core Facility at the University of Utah put together an Arduino-based solution to get proper bright-field illumination in an OpenSPIM setup: [Brightfield](Brightfield).

# Shutter

Instructions to make an Arduino-controlled shutter compatible with uManager: [paper by Todd P. Meyrath](http://george.ph.utexas.edu/~meyrath/informal/shutter.pdf) and [tutorial on the uManager page](https://micro-manager.org/wiki/Control_laser_shutters_with_Arduino).

# Stepper Motor Upgrade

[If you would like to swap out one of the Picard stepper motors you can do so with a bit of effort.](https://openspim.org/Stepper_Motor_Upgrade)


# OpenSPIM for large samples

## Field of view

The original OpenSPIM uses a 2X expander to enlarge the laser beam to 2 mm. For larger samples a larger field of view can be preferable. This means that you will need a larger beam to create a taller light sheet. Change the second beam expander lens to f=75 mm or 100 mm and increase the distance between lenses accordingly.

## Objectives

Immersion objectives with long working distance are hard to find. However, at low NA and moderate magnification, a dry objective will also work; the higher NA, the more spherical aberrations will be present. Keep in mind that when using a dry objective in immersion, the WD will increase (approximately by a factor equal to the RI of the new medium, eg. 17 mm in air will increase to 22.6 mm in water).

## Example parts list

The table below lists the parts used by the OpenSPIM for brains setup built by Monika Pawłowska (Nencki Institute of Experimental Biology, Warsaw).

<table>
<tr class="header">
<th>Manufacturer</th>
<th>Accessibility</th>
<th>Description</th>
<th>File or Link/Model #</th>
<th>Image</th>
<th>Quantity</th>
<th>Price (EUR)</th>
</tr>
<tr class="odd">
<td>Nikon</td>
<td align="center" bgcolor="pink">purchase</td>
<td>4X Nikon Plan Fluorite Imaging Objective, 0.13 NA, 17.2 mm WD, dry</td>
<td><a href="https://www.thorlabs.de/thorproduct.cfm?partnumber=N4X-PF">N4X-PF</a></td>
<td align="center"><img src="images/Thorlabs_N4X-PF_objective.jpg" width="50%"></td>
<td align="center">2 (or 3 for double illumination)</td>
<td align-"center">410</td>
</tr>
<tr class="even">
<td>Thorlabs</td>
<td align="center" bgcolor="pink">purchase</td>
<td>Translating Lens Mount for Ø1" Optics (for the objectives)</td>
<td><a href="https://www.thorlabs.de/thorproduct.cfm?partnumber=LM1XY/M">LM1XY/M</a></td>
<td align="center"><img src="images/Thorlabs_LM1XY_mount.jpg" width="50%">
<td align="center">2 or 3</td>
<td align="center">125</td>
</tr>
<tr class="odd">
<td>Nikon</td>
<td align="center" bgcolor="pink">purchase</td>
<td>Infinity-Corrected Tube Lens for Plan Fluorite Objectives</td>
<td><a href="https://www.thorlabs.de/thorproduct.cfm?partnumber=ITL200">ITL200</a></td>
<td align="center"><img src="images/Thorlabs_ITL200_lens.jpg" width=50%"></td>
<td align="center">1</td>
<td align="center">405</td>
</tr>
<tr class="even">
<td>Monika</td>
<td align="center" bgcolor="green">self made</td>
<td>This chamber can be 3D printed. For windows use 24x24 mm microscopy cover glasses and glue (eg. two component epoxy)</td>
<td><a href="https://github.com/openspim/openspim-parts/blob/master/Chambers/Dry_Objectives_Chamber_and_Holder/Chamber.stl">Chamber.stl</a></td>
<td align="center"><img src="images/Large_samples_chamber_3D.PNG" width="50%"></td>
<td align="center">1</td>
<td></td>
</tr>
<tr class="odd">
<td>Monika</td>
<td align="center" bgcolor="green">self made</td>
<td>This holder includes two threaded holes so it's easiest to make from metal (eg aluminum). Holder is mounted on the 4D stage arm with M6 screw. Glass slide with 1 mm thickness can be held with nylon or nylon-tipped screw</td>
<td>
<a href="https://github.com/openspim/openspim-parts/blob/master/Chambers/Dry_Objectives_Chamber_and_Holder/Metal_Holder.pdf">Metal_Holder.pdf</a><br/>
<a href="https://github.com/openspim/openspim-parts/blob/master/Chambers/Dry_Objectives_Chamber_and_Holder/Metal_Holder.step">Metal_Holder.step</a></td>
<td align="center"><img src="images/Holder.PNG" width=40%></td>
<td align="center">1</td>
<td></td>
</tr>
</table>
