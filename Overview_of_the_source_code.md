---
title: Overview of the source code
layout: page
description: OpenSPIM software overview
---
OpenSPIM's software is embedded into [µManager](https://micro-manager.org/) and [Fiji](https://fiji.sc/).

Our modifications are maintained on [GitHub](https://github.com/openspim/micromanager/). The additional vendor libraries are maintained in our [fork](https://github.com/openspim/3rdpartypublic) of µManager's *3rdpartypublic* repository of binary libraries and documentation.

# Overview of the µManager source code

µManager is divided into the following parts:

1.  the core. Written in C++, lives in *MMCore/*. Has basic helper functions (logging, library loading, etc).
2.  the device base. Also written in C++, lives in *MMDevice/*. Has the abstract definitions of the devices µManager understands.
3.  the device drivers. They live in *DeviceAdapters/* and most of them require additional third-party libraries from the hardware vendors.
4.  the Java binding. Uses [SWIG](https://www.swig.org) to define the interface to MMCore, lives in *MMCoreJ\_wrap/*.
5.  the ImageJ plugin *Micro-Manager Studio*. Written in Java, lives in *mmstudio/*.
6.  the µManager plugins. These implement the interface *org.micromanager.api.MMPlugin* and must reside inside .jar files in *\<ij.dir\>/mmplugins/* after being compiled. The sources live in *plugins/<jarname>/*.
7.  the 3rd-party libraries. Some of those are helpfully made public by the hardware vendors and live in the directory *../3rdpartypublic/*, i.e. **outside** the µManager source code. Those libraries which non-disclosure agreements or similar niceties prevent from being redistributed live in *../3rdparty/*. Evidently, the µManager developers have an internal repository for this, as do the Dresden and Madison OpenSPIM developers.

# Overview of the OpenSPIM software

OpenSPIM's additions and enhancements to µManager are divided into three parts:

  - additional hardware drivers
  - some plugins (mainly the GUI, but also time-lapse acquisition)
  - some cleanups

## Additional hardware drivers

We added a *PicardStage* driver (called *DeviceAdapter* by µManager). This driver is written in C++, like all DeviceAdapters in µManager, and lives in the [*DeviceAdapters/PicardStage/*](https://github.com/openspim/micromanager/tree/openspim/DeviceAdapters/PicardStage/) subdirectory. It implements an XY stage, a Z stage and another 'stage' for the rotation device (called *twister* by Picard systems).

Our [*dc1394* driver](https://github.com/openspim/micromanager/tree/openspim/DeviceAdapters/dc1394/) adaptation for 32-bit Windows has been [merged upstream](https://github.com/openspim/micromanager/commits/svn/git-svn/DeviceAdapters/dc1394) and [integrated into the default Windows 32-bit build](https://github.com/openspim/micromanager/commit/1301411b14d35ede4f46b71e39574b86086517f3).

## OpenSPIM plugin

The majority of the OpenSPIM software is implemented as the *OpenSPIM plugin* for µManager. It is written in Java and lives in the [*plugins/SPIMAcquisition/*](https://github.com/openspim/micromanager/tree/openspim/plugins/SPIMAcquisition) subdirectory.

### Stage control

Since the stage has no physical knobs you can turn to position the sample, we needed to implement our own, fine control. It is available in the [*Stage Controls*](Operation#Stage_Control) tab of the OpenSPIM GUI and implemented in the *SPIMAcquisition* class, using a couple of additional classes to implement recurring GUI elements, e.g. *IntegerField*, *IntegerSlideField*, *MotorSlider* and *MappedMotorSlider*.

### Live Window hack

The OpenSPIM plugin also uses a hack that allows us to intercept user input to µManager's Live Window so that holding down the *Alt* key and moving the mouse horizontally will rotate the sample -- if the rotation axis has been calibrated properly, the plugin will compensate X and Z so that the rotation is in effect around the center of the field of view rather than the physical rotational axis.

### Acquisition engine

Extending the default acquisition engine is difficult, due to µManager's acquisition engine having been implemented in the rather obscure language Clojure. This precludes the addition of features such as an additional dimension (the angle), anti-drift and OME-TIFF output. As such, we had to reinvent the acquisition engine in pure Java; our source code lives in the [*spim.progacq*](https://github.com/openspim/micromanager/tree/openspim/plugins/SPIMAcquisition/spim/progacq) package of the *SPIMAcquisition* plugin and we welcome enhancements (excepting only a port to Clojure).

### Calibration of the rotational axis

Obviously, it is very rare that the rotation axis defined by the Picard twister happens to coincide with the center of our specimen. To that end, we implemented two calibration methods to determine the physical rotation axis (implemented in the *SPIMAutoCalibrator* and *SPIMManualCalibrator* classes). This allows us to simulate a rotation around the center of the field of view by compensating for the location of the real axis using the X and Z motors. For additional eye-candy (which turned out to be quite useful for debugging) we can visualize the calibration steps using Fiji's [3D Viewer](https://fiji.sc/3D_Viewer).

### Anti-Drift

In real life, there is always a little drift, whether it be the Agarose column stretching due to its own weight or the specimen moving on its own accord or something else yet. Obviously, we need to address that drift for long-term time-lapse recordings. After testing quite a couple of methods, we settled for the following strategy: while saving the files (so as to interfere as little as possible with the acquisition process), we calculate XY, XZ and ZY projections on the fly. By using the phase correlation provided by the [ImgLib](https://github.com/imagej/imglib/) library included in Fiji, we get two values for X, Y and Z drift, each. We average those values to initialize the drift correction.

For manual inspection -- and for interactive correction, should the phase correlation fail -- we show the overlayed projections in a window where the user can correct them using the arrow and page up/down keys.

Both the phase correlation and the GUI of the anti-drift are implemented in the *ProjDiffAntiDrift* class.

### Asynchronous writing

By profiling the acquisition code, it was discovered that the process of writing out each slice to its appropriate file took nearly 60% of the total acquisition time. To remedy this, asynchronous output handling was added by way of the *AsyncOutputWrapper* class. This class wraps any other output handler (most usefully, the OME-TIFF output handler) and rather than writing each image as it is recorded, the slices are queued up and handled by a separate thread. This allows the motor movements and acquisition to resume while the file is written in the downtime (i.e. in between time points).

### OME-TIFF

As most datasets are far too large to store in memory, we wrote the *OMETIFFHandler* class to handle output from acquisition. As an open file format designed for microscopy, OME-TIFF was the logical choice. The files are written using the Bio-Formats library (with some temporary modifications to account for some unusual issues we encountered; see our [Bio-Formats](https://github.com/openspim/bioformats) fork).
