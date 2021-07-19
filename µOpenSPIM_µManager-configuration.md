##	Creating a working .cfg file using µManager's Hardware Configuration Wizard

The following video shows how a working .cfg file was created from scratch for the described [X-OpenSPIM](/Table_of_parts_X-OpenSPIM) using µManager's Hardware Configuration Wizard.</br>

<a href="https://openspim.org/videos/SettingUp_MM.mp4" target="_blank" title="MultiCamera"><img src="https://openspim.org/videos/SettingUp_MM.gif" width="300" alt="Configuring two Andor sCMOS cameras with µManager." /></a>

## Configuring multiple cameras in µManager (X-OpenSPIM)
This video demonstrates how to configure two sister cameras (2x Andor sCMOS Neo 5.5) in µManager to function as a single logical camera (Multi-Camera).</br> 
<a href="https://openspim.org/videos/SettingUp_MultiCamera.mp4" target="_blank" title="How to create a .cfg file using µManager's Hardware Configuration Wizard"><img src="https://openspim.org/videos/SettingUp_MultiCamera.gif" width="300" alt="Creating a .cfg file using µManager's Hardware Configuration Wizard." /></a></br>

## Pixel size calibration
It is also important to calibrate your Pixel Size correctly. To do this in µManager go to *Devices* > *Pixel Size Calibration* and specify the Pixel Size (µm). Before you can  *OK*, you have to select at least one of the devices from the "Property Name" table, e.g. Core-Initialize. Now click *OK* and save/overwrite the current configuration file.</br>

If you don't know the correct Pixel Size value for your OpenSPIM system check:

-	the Pixel Size of your camera chip
-	the magnification of your detection objective (e.g. 10x, 20x, 40x etc.)
-	if the detection axis is equipped with any other demagnifying lenses (e.g. C-mount) or zoom optics. </br>In case of the described [X-OpenSPIM](/Table_of_parts_X-OpenSPIM), the [camera mounts & adapters](https://openspim.org/images/%C2%B5OpenSPIM/CameraAdapter/CameraAdapterExploded.png) comprising a tube lens (ITL200, Thorlabs), a U-TV1x video camera adapter (projection lens) and a U-CMAD3 video camera mount adapter retain a 1x magnification.

Once you gathered the information the following formula can be used:</br>
</br>
<p align="center">+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++</p>
<p align="center">Image Pixel Size = Camera Pixel Size x Binning / Magnification of the Detection Objective x Camera Mounts x Zoom Optics</p>
<p align="center">+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++</p></br>

As an example:</br>
Our two Andor sCMOS Neo 5.5 cameras have 6.5 µm pixels and the X-OpenSPIM is equipped with 40x detection objectives (CFI Apochromat NIR 40X W, Nikon). Camera mounts retain a 1x magnification and there are no additional zoom optics installed into the detection axis.</br>

Therefore we have a Image Pixel Size of 6.5 x Binning / 40 x 1 x 1, which equals a Pixel Size value of 0.1625 µm.</br>
We don't worry about the Binning as µManager is taking this automatically into account.

## Setting up an Arduino microcontroller in µManager
A detailed description on how to configure and set up an ArduinoUNO board for hardware controlled imaging with µOpenSPIM is coming soon.</br>
You can already watch the video below to see how we configure an ArduinoUNO board for camera-laser synchronization in an OpenSPIM.</br>
<a href="https://openspim.org/videos/SettingUp_ArduinoUNO.mp4" target="_blank" title="How to create a .cfg file using µManager's Hardware Configuration Wizard"><img src="https://openspim.org/videos/SettingUp_ArduinoUNO.gif" width="300" alt="Creating a .cfg file using µManager's Hardware Configuration Wizard." /></a>