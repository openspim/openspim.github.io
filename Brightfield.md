---
---
Strategies to implement a proper brightfield illumination in an OpenSPIM.

## Michael Redd's solution

### parts

  - 20 cent green diode
  - Arduino
  - 10K potentiometer
  - 100 Ohm resistor

### setup & wiring

The Arduino and light are powered by USB and are turned on and off by micro-manager and can be used as a brightfield channel in micromanager multi-dimensional acquisition window. The potentiometer and resistor determine the intensity of the light. The diode is fixed in place behind a collimating lens which fills the back aperture of a 10x immersion lens on axis with the sample and imaging lens. If your SPIM rig does not have a appropriate port and/or you do not have the 10x lens, one could focus the diode on the sample from above at an oblique angle. This may require a brighter light, but would probably work with the diode I am using. Light level can be dialed in by using different resistors and potentiometers.

by Michael Redd, Cell Imaging Core Facility, University of Utah

{% include image src="Redd_brightfield.png" width="70%" caption="Setup" %}

{% include image src="Redd_brightfield2.png" width="70%" caption="Wiring" %}
