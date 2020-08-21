---
---
## Materials

##### Objects needed

  - 1x Test grid/mirror sample (described below)

##### Tools needed

  - 1x Pencil with eraser.

##### How to make the test grid

To calibrate the light-sheet, a broken-up test slide such as

  - [Edmund Optics Opal Glass Ronchi Ruling Slide](https://www.edmundoptics.com/testing-targets/test-targets/resolution-test-targets/opal-glass-ronchi-ruling-slides/2838)
  - [Edmund Optics Multi-Grid Standard Stage Micrometer](https://www.edmundoptics.com/testing-targets/test-targets/image-analysis-test-targets/multi-grid-standard-stage-micrometer/58-607)

can be used. Typically, you would glue it to a sample holder (for which we use a Braun Omnifix-F 1 ml syringe):

{% include image src="Edmundoptics_58607_broken.jpg" width="70%" caption="Slide after \"extraction\" of the 2.0mm (100μm divisions) part" %}
{% include image src="Light_Sheet_Calibration-1.jpg" width="70%" caption="Overview of the sample holder & grid" %}
{% include image src="Light_Sheet_Calibration-2.jpg" width="70%" caption="Close-up to the bottom part" %}
{% include image src="Light_Sheet_Calibration-3.jpg" width="70%" caption="Bottom part, magnified" %}
{% include image src="Light_Sheet_Calibration-4.jpg" width="70%" caption="Close-up of the bottom part, magnified" %}

## Method

### 1. Determine sample chamber position

{% include video id="iWarKfx4hTI" width="400" height="243" caption="" %}

  First one must align the OpenSPIM chamber along the detection axis until it is in line with the illumination axis. This assures that the laser is roughly entering in the middle of the back aperture of the 10x/0.3 NA water dipping illumination objective lens. One can see the effects on the light sheet position very easily by observing how the light exits the front of the objective lens into the water. Try and get it to come out parallel to the illumination axis, and perpendicular to the detection axis.

### 2. Position the grid/mirror sample in the field of views

{% include video id="xkLd8U-fO6E" width="400" height="243" caption="" %}
{% include video id="7LYBt_2Mu3Q" width="400" height="243" caption="" %}

  Suspend the test grid/mirror sample in the OpenSPIM sample chamber in front of the 20x/0.5 NA water dipping detection objective lens with its grid facing in the direction of the camera.

### 3. Focus the grid/mirror sample, and position it in θ

{% include video id="m1enyaG-FGM" width="400" height="243" caption="" %}
{% include video id="o8EBKwrS354" width="400" height="243" caption="" %}

  Once the grid/mirror sample has been roughly positioned in front of the detection objective, bring it in to focus with the Z-axis of the USB-4D-Stage. After it is in focus and known to be roughly flat across the field of view, rotate it 45 degrees toward the illumination objective. Finally position the sample and focus on a feature on the patterned grid/mirror. This 45 degree orientation makes it possible to bounce the laser coming out of the illumination objective directly into the detection objective.

### 4. Replace the emission filter with an ND filter

{% include video id="yAMg_7_niQ4" width="400" height="243" caption="" %}

  An ND filter should be used in either the illumination path or detection path due to the high power of the laser. The intensity of the light could damage the system's camera or over-saturate the image.

### 5. Adjust the focus of the second lens of the telescope

{% include video id="8aTdHjbEEds" width="400" height="243" caption="" %}
{% include video id="bW6wjXkxmNM" width="400" height="243" caption="" %}
{% include video id="FGKImtkj8lc" width="400" height="243" caption="" %}

  Unscrew the thumbscrew for the second lens of the telescope system, then using a pencil with a rubber eraser push/roll it back or forth along the dovetail rail to find the correct position. It is really imperative in this step to have a sample in focus (for example, specimen or the test grid/mirror).

### 6. Adjust the position of the light sheet so that is is in the focal plane of the detection lens

{% include video id="rr6yKCXWbpE" width="400" height="243" caption="" %}

  Adjust the mirror mount on the post with the horizontal knob so that the laser light sheet is over top the focal plane of the detection lens.

### 7. Adjust the orientation of the cylindrical lens

{% include video id="4_uhdUIPuBI" width="400" height="243" caption="" %}
{% include video id="4V53F6ecg04" width="400" height="243" caption="" %}

  Using the indexed rotation mount, rotate the cylindrical lens to where it is focusing it's light horizontally on the mirror. One can also look at back reflections on the vertical variable slit.
