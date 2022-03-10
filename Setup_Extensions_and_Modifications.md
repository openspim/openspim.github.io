---
title: Setup Extensions and Modifications
layout: page
description: Additional setup tweaks
---
## Bright-field illumination

Michael Redd from the Cell Imaging Core Facility at the University of Utah put together an Arduino-based solution to get proper bright-field illumination in an OpenSPIM setup: [Brightfield](Brightfield).

## Shutter

Instructions to make an Arduino-controlled shutter compatible with uManager: [paper by Todd P. Meyrath](http://george.ph.utexas.edu/~meyrath/informal/shutter.pdf) and [tutorial on the uManager page](https://micro-manager.org/wiki/Control_laser_shutters_with_Arduino).

## Stepper Motor Upgrade

[If you would like to swap out one of the Picard stepper motors you can do so with a bit of effort.](https://openspim.org/Stepper_Motor_Upgrade)


## OpenSPIM for large samples

## Field of view

The original OpenSPIM uses a 2X expander to enlarge the laser beam to 2 mm. For larger samples a larger field of view can be preferable. This means that you will need a larger beam to create a taller light sheet. Change the second beam expander lens to f=75 mm or 100 mm and increase the distance between lenses accordingly.

## Objectives

Immersion objectives with long working distance are hard to find. However, at low NA and moderate magnification, a dry objective will also work; the higher NA, the more spherical aberrations will be present. Keep in mind that when using a dry objective in immersion, the WD will increase (approximately by a factor equal to the RI of the new medium, eg. 17 mm in air will increase to 22.6 mm in water).

## OpenSPIM for brains setup

[Click here for a table that lists the parts used by the OpenSPIM for brains setup built by Monika Pawłowska (Nencki Institute of Experimental Biology, Warsaw).](https://openspim.org/OpenSPIM_for_brains_setup)

## X-OpenSPIM example equipped with two laser lines and a cooling chamber

A [detailed description of how an OpenSPIM can be upgraded](https://openspim.org/x-openspim_welcome) to contain a second illumination axis with two cameras and multiple laser lines under the control of an Arduino board. The system also features a cooling chamber.