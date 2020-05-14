# Development with IntelliJ

## Setup

  - install JDK 8 (or earlier, JDK 6 is best if you want to be
    compatible with all OpenSPIM installations) from
    <http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html>
  - install the latest Fiji version *without JRE* from
    <http://fiji.sc/Downloads#Fiji>
  - install IntelliJ from <http://jetbrains.com>
  - start Fiji and add the MicroManager-dev update site via *Help \>
    Update... \> Manage Update Sites \> Add* - the address of the update
    site is <http://sites.imagej.net/Micro-Manager-dev/>
  - restart Fiji to install the MicroManager components fully.

## SPIMacquisition source code and import

  - acquire the SPIMAcquisition source code via git clone from
    <https://github.com/openspim/spimacquisition>
  - import the folder you just cloned into IntelliJ as a Maven project.
  - in the Module settings (reachable via right-click on the project or
    by pressing `F4`), add both directories `[Fiji]/jars` and
    `[Fiji]/plugins/Micro-Manager` to *Global Libraries*.
  - in the Module settings, go to *Artifacts* and add a *JAR* artifact
    with *From modules with dependencies*. Choose SPIMacquisition as
    main class.
  - the module is now ready to build - click *Build \> Make Project* or
    *Build \> Build artefacts...* - the output JAR will be put in the
    folder `out/artifacts/SPIMacquisition_JAR` with the name
    `SPIMacquisition.jar` - you can copy this file then to
    `[Fiji]/mmplugins` and use it in MicroManager.

## Debugging with IntelliJ and VisualVM

*TODO*
