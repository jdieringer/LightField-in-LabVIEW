LightField-in-LabVIEW
=====================

A library for automating Lightfield from Princeton Instruments using National Instruments LabVIEW.

Current To-Do List

-Add spectrometer support
-Add emCCD support
-Add emICCD support
-Create a series of example VIs for various use cases
-Test automation from 32-bit LabVIEW for LightField 4.8+

Revision History

9/8/2014
-Values for settings are now tested by LightField and a popup is set if the value is out of range.
	Popup will be changed to an error in a future release.
-Trying to set a property that is not valid for the current configuration will no longer crash 
	LightField. A popup message is displayed instead. Popup will be changed to an error in a future
	release.
-Rewrote all camera setting class VIs to use an generic Read/Write setting advanced VI. The generic
	Read/Write VIs can be used to to set properties that are not yet implemented elsewhere.
-Added a psuedo client-server mode for faster testing. The server runs and exports the class object
	in a global variable. VI's can pull this global and interact with LightField without 
	initializing a new instance during each run of the VI. A more robust implementation may be 
	developed in the future, but this was mostly done to speed up development of the library.

8/27/2014
-Added ICCD support for the following functions: Aux Out Delay/Width, Gate Mode (Rep or Seq), 
	Intensifier Gain, Internal Trigger Frequency, On Chip Accumulations, Rep Gate Delay/Width, 
	Seq Start and End Delay/Width
-Reorganized Class VI structures
-New icon theme for future expansion
-Added SPE parsing functions implemented in native LabVIEW for faster data transfer under
	special conditions (large frame numbers).
-Moved repository to github.com
	
8/11/2014
-Initial release of proof of concept VI's for testing. Only CCD support implemented