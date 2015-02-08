
      Northrop T-38 Talon (JSBSim Model)

Version 1.2, released 16 October 2003

Configuration files for the FlightGear flight simulator
www.flightgear.org <http://www.flightgear.org/>.
By David Culp, April 2003, davidculp2@attbi.com
<mailto:davidculp2@attbi.com>
License: GPL (see http://www.gnu.org/licenses/gpl.html)

------------------------------------------------------------------------


      Overview

This is a first attempt at using a single archive to distribute all the
files needed to model an aircraft in FlightGear. This archive should be
extracted into directory $FGROOT/Aircraft/T38. The engine file will then
need to be moved to the $FGROOT/Engine directory. Eventually FlightGear
will be able to keep all the files for an airplane in one directory.

------------------------------------------------------------------------


      Contents

filename 	description 	placement
T38-read-me.html 	This Readme file 	$FGROOT/Aircraft/T38
T38.xml 	The flight model 	$FGROOT/Aircraft/T38
T38-set.xml 	An alias for the main configuration file 	$FGROOT/Aircraft/T38
T38-jsbsim-set.xml 	The main configuration file 	$FGROOT/Aircraft/T38
T38-sound.xml 	The sound configuration file 	$FGROOT/Aircraft/T38
T38-electrical.xml 	The electrical system (unused) 	$FGROOT/Aircraft/T38
J85-GE-5_sim.xml 	The engine configuration file 	$FGROOT/Engine
t38 	A Unix/Linux shell script for fgfs 	~


directory name 	description 	placement
Sounds 	Contains .wav files and sound configuration for the T-38
$FGROOT/Aircraft/T38
Panels 	Contains the T-38 instrument panel configuration
$FGROOT/Aircraft/T38
Models 	Contains the T-38 3D model 	$FGROOT/Aircraft/T38
Instruments 	Contains T-38-specific instruments 	$FGROOT/Aircraft/T38


------------------------------------------------------------------------


      Bugs

I'm still fairly new to FlightGear, so some of these "bugs" may actually
be features :)

bug 	status
3D model has some bugs 	The model is a reskinned version of the Captain
Slug AT-38, with modifications by Innis Cunningham, who converted the
model from MDL to AC3D format and added animations and a cockpit. There
are missing gear doors. It could use gear sequencing. Some texture
missing from aft fuselage.
The ADI falls apart above about +/-20 degrees of pitch 	Texture cropping
is not available yet for 2D cockpits
The instrument panel is too small 	This is actually a feature :) It is
meant to increase visibility over the nose.
T-38's don't have that instrument at the right side of the panel 	That's
for flight test only. If you don't want it there just comment out the
"Aero data" instrument in T38-panel.xml.
Where's the cheezy AOA Christmas tree? 	Ignored for now.
The VOR doesn't work 	Working on it.
The altimeter digital readout is out of sync 	Rounding error. A
'truncate' unary operator is needed.


------------------------------------------------------------------------


      Flying the T-38

Apply full throttle, afterburner is optional but recommended until 300
knots. Rotate at 140 knots . When airborne raise gear and flaps
immediately. Be carefull not to sink after initial flap retraction.
Climb at a shallow angle, less than 1000 fpm, until reaching 300 knots,
then climb at 300 knots to 0.8 Mach. To land fly downwind at 300 knots
clean, on base slow to 200 knots, extending gear and half flaps passing
through 220 knots. On final extend full flaps and slow to 160 knots.

I recommend using the "hat switch" on your joystick to control
stabilizer trim. I know most people like to use it for view changes, but
you can't fly a jet without lots of stab trimming.

Let me know if you'd like more features, and if you have recent time in
the T-38 let me know if this model flies reasonably close to the real
airplane.


      Notes

The engine model uses the FGSimTurbine module of JSBSim. The afterburner
can be activated in one of two ways, as defined by the AUGMETHOD value
in the engine configuration file.

The "AOA buffet" sound activates at an AOA of 5.7 degrees. The sound
should be a lower frequency buffet, and maybe I'll find the right sound
someday. As far as the activation AOA, it's only a guess.

The light in the gear handle activates whenever throttle[0] is at idle
and the gear handle is up. Not exactly how it works in the real
airplane, but close.



------------------------------------------------------------------------
16 Oct 2003
