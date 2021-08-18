##	Creating a working .cfg file using µManager's Hardware Configuration Wizard

The following video shows how a working .cfg file was created from scratch for the described [X-OpenSPIM](/Table_of_parts_X-OpenSPIM) using µManager's Hardware Configuration Wizard.</br>

<a href="https://openspim.org/videos/SettingUp_MM.mp4" target="_blank" title="MultiCamera"><img src="https://openspim.org/videos/SettingUp_MM.gif" width="300" alt="Configuring two Andor sCMOS cameras with µManager." /></a>

## Configuring multiple cameras in µManager (X-OpenSPIM)
The following step by step guide and example video demonstrate how to configure two sister cameras (2x Andor sCMOS Neo 5.5) in µManager to function as a single logical camera (Multi-Camera).The configuration is facilitated by the fact that both cameras are of the same type.</br> 
<a href="https://openspim.org/videos/SettingUp_MultiCamera.mp4" target="_blank" title="How to create a .cfg file using µManager's Hardware Configuration Wizard"><img src="https://openspim.org/videos/SettingUp_MultiCamera.gif" width="300" alt="Creating a .cfg file using µManager's Hardware Configuration Wizard." /></a></br>

-	Step 1:
Because both Andor cameras use the same device adapter, they can be added and named through the “Hardware Configuration Wizard” by selecting successively the “AndorSDK3” option within the folder of the same name from the list of available devices. Thereby the camera, which is initially added, should be considered the “slave” camera, whereas the second camera becomes the “master”. In case the two cameras are not of the same type, they must at least have the same width, height and pixel type properties.

-	Step 2:
Use the “Hardware Configuration Wizard” to add the “Multi Camera” option, which is also located in the device list and can be found within the “Utilities” folder. Complete and save the “Hardware Configuration Wizard” comprising all other hardware components including lasers, 4D-stage and the ArduinoUNO board.

-	Step 3:
Create a new “Group” within µManager’s configuration settings named “System”. This step is necessary to specify the physical camera properties. To do so, one has to go into the Group Editor by pressing the Group “Edit” button and tick the Multi Camera-Physical Camera 1 and Multi Camera-Physical Camera 2 from the Property Name list. Furthermore, the “Core-Camera”, “Binning” and “TriggerMode” has to be added for both cameras and confirmed with OK.

-	Step 4:
Now is the time to edit all preset values of our newly created “System” group. Press the ”Edit” button of the preset panel. In there one can specify the Andor sCMOS Camera-1 as Multi Camera-Physical Camera 1 and Andor sCMOS Camera-2 as Multi Camera-Physical Camera-2. Additionally, the “TriggerMode” of Camera-1 (the ‘Slave’) has to be set to “External” and of Camera-2 (the ‘Master’) to “Internal (Recommended for fast acquisition)”. Subsequently we recommend to set both Cameras to 2x2 binning. All above mentioned preset values are shown in the figure below.

-	Step 5:
Furthermore, we advise to follow µManager’s “Multi-Camera” recommendations and set the preset name to “Startup” as this will automatically set all Properties within the “System”-Group to any given preset value during µManager’s startup.
At this point the configuration settings for the two cameras are completed and can be saved.

-	Step 6:
Finally, the “Multi Camera” of µManager’s Core Camera Utility has to be selected in the Device Property Browser before a single multi-channel image (1 channel per camera) can be acquired.
To shorten this step, we added another group by selecting the Utility “Core Camera”. This allowed us to quickly switch between Camera 1, Camera 2 and Multi Camera within the “Configuration Settings”.
</br>
For multi camera imaging we recommend using a decent acquisition computer. E.g., we use a HPZ820 workstation with multiple processors and, notably, found that enabling the non-uniform memory access (NUMA) in the BIOS greatly improves image acquisition stability.

<a href="https://openspim.org/images/ConfigCameras.png" target="_blank" title="Configuring the MultiCamera in µManager"><img src="https://openspim.org/images/ConfigCameras.png" width="800"><figcaption>Multi camera “Startup” preset values of the newly created “System” configuration group in µManager.</figcaption></a>


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
The following steps depict how an ArduinoUNO board can be configured to enable hardware-controlled triggering of two laser lines (in our case a 488 and 561 laser; see also Figure 23).
If one is not yet familiar with µManager’s Hardware Configuration Wizard, its Device Property Browser and how to create Configuration “Groups” and “Presets”, we recommend first reading through µManager’s [Configuration Guide](https://micro-manager.org/wiki/Micro-Manager_Configuration_Guide).
</br>
You can also watch the video below to see how an ArduinoUNO board is configured for camera-laser synchronization in an OpenSPIM.</br>
<a href="https://openspim.org/videos/SettingUp_ArduinoUNO.mp4" target="_blank" title="How to create a .cfg file using µManager's Hardware Configuration Wizard"><img src="https://openspim.org/videos/SettingUp_ArduinoUNO.gif" width="300" alt="Creating a .cfg file using µManager's Hardware Configuration Wizard." /></a>



