## Software versus Hardware controlled imaging

“Software controlled” indicates that during image acquisition the software itself (e.g. µManager) controls all hardware components of the microscope, such as camera exposure times, filter wheels, the 4D-stage, and laser shutters. In this case acquisition remains relatively slow in comparison to microscopes, where some or most of the hardware components are controlled using triggering signals.
If slow developmental processes are captured, where imaging speed plays a subordinate role, software controlled acquisition may be sufficient.</br>
 
An ArduinoUno board allows to speed up acquisition speed by connecting the board’s digital output pins to hardware components of the OpenSPIM system. As shown in the figure below one can connect two of the Arduino output pins directly to two separate laser lines whereby the Arduino shutter takes over the laser shutter, which would be controlled by the Software. As a result, the lasers will fire faster and more synchronously with the camera's exposure time, benefiting acquisition speed and making illumination more precise.
It is important to note that µOpenSPIM assumes that the camera will be connected to the Arduino board and therefore provides the initial 5V TTL-trigger-pulse.

If yo would like synchronize your laser or multiple laser lines with the camera exposure follow this link for more information on [how to configure µManager for an ArduinoUNO board](/µOpenSPIM_µManager-configuration).