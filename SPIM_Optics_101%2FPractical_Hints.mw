== Beam plane ==
'''Typically all optical beams of a setup should be in one plane parallel to the table top.'''

This principle makes the whole setup predictable and safe, as everybody always knows where to expect (possibly dangerous) light. Also it makes it easier to install laser shielding (e.g. a wall around the setup). 

A simple means to achieve this goal is by defining the beam height before starting to build the setup. This can be done by mounting an iris or alignment disc with its hole on the desired beam hight. Then this tool can be used for any further alignment.

== Kinematic mirror mounts ==
[[File:Spimoptics kinematicmirrormount.png|thumb|300px|kinemtic mirror mount]]
The mirrors in the OpenSPIM are all mounted in kinematic mirror mounts. These mounts allow to flap the mirror around two perpendicular axes:
# Moving knob SB will flap the mirror around the axis defined by knobs ST and SC. This will move the beam left/right (green line).
# Moving knob ST will flap the mirror around the axis defined by knobs SB and SC. This will move the beam up/down (blue line).
# The mirror may be shifted, if all knobs are moved (bottom right in figure).
'''Note''' that with these mirror mounts the rotation axis of the mirror is NOT IN THE CENTER of the mirror. So flapping a mirror will always lead to a parallel shift of the reflected beam, as the reflection point moves (see bottom left figure).
Due to the size of the mirror mount the shift of the reflection point is typically not very large and can be mostly neglected.

== Aligning a laser beam in space ==
[[File:Spimoptics alignmentinspace.png|thumb|400px|alignment of a laser beam in space]]
Each laser beam (in space) is defined by four free parameters (a position x,y on a plane in space and a direction defined by two angles). This can be seen in the figure (A) on the right, where all beams hit the same point on a plane (2), but only the green beam is parallel to the z-axis. So to align a laser beam in space (e.g. parallel to an optical rail, as in the OpenSPIM), it needs to go through two points in space (e.g. two alignment discs or irises).

Figure (B) on the right shows a typical setup to align a laser beam in space. It uses two mirrors M1 and M2 (on kinematic mounts, i.e. with two degrees of freedom each) and two alignment discs or irises (targets T1 and T2). In the OpenSPIM this appears e.g. with the two mirrors directly behind the laser, which allow to align the beam parallel to the optical rails. To align the beam, follow these steps:
# Roughly align the mirrors, so the beam is not too far from its ideal position.
# Align mirror M1, so the mirror passes T1. Now it will maybe NOT pass T2
# Use mirror M2 to make the beam hit T2 (which might make the beam miss T1). If you use irises, open up iris T1 so the beam passes until T2.
# Return to step 2 and iterate this process until the beam passes through the centers of T1 and T2.
The crucial point here is to use the first mirror to align on the first target and the second mirror for the second target.


== Estimating the focal length of a lens ==
There is an easy way to estimate the focal length of a lens. You will need a far away light source (e.g. a lamp at the other end of the room) and a white wall or sheet of paper. 
# Hold the lens a short distance in front of the paper or wall and change the distance until you see a sharp image of the light source. 
# Now measure the distance between the lens and the screen. This distance will roughly equal the focal length. The estimate is the better, the smaller the focal length is, compared to the distance to the light source.


[[Category:SPIM Optics 101]]
