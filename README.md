# Toga Snap!

This is the code from the [PyBeeWare](https://beeware.org/) 
[Briefcase](https://github.com/beeware/briefcase) 
[tutorial](https://briefcase.readthedocs.io/en/latest/tutorial/getting-started.html),
with the addition of a `snapcraft.yaml` file so that the Converter
application can be run as a Snap in Linux!

A lot of the work figuring out the Snapcraft yaml was done by 
[@Stephan-kashkarov](https://github.com/Stephan-kashkarov).

Disclaimer: I do not fully understand everything here, this is just
a proof of concept to find a working starting point for future work in 
getting Briefcase to build Snaps. If you do not know what I'm talking
about, please go see the [Beeware project](https://beeware.org/)!

### Building and installing the snap

These instructions have been tested on Ubuntu 18.04

In the root folder of this project:

0. `sudo apt install snapcraft` (only if snapcraft is not installed)
1. `snapcraft` (may take 5-10 minutes or more depending on internet 
   speed, this creates a vm and installs *everything*)
2. `sudo snap install --devmode --dangerous *.snap`

### Running the snap

`converter-pybee`

### Uninstalling and cleaning

To uninstall the snap:

`sudo snap remove converter-pybee`

To clean up the build artifacts, in the root folder of this project:

`snapcraft clean`

## Next steps

- Can you make a nice little shortcut without having to add the app to
  the Snap store?
- Is there any further work required before the app could be [added to
  the Snap store](https://snapcraft.io/docs/releasing-your-app)?
- Make Briefcase generate the `snapcraft.yaml`
- Look into whether this current configuration works across a variety
  of Linux distributions, versions, and systems or if further 
  investigation is required
  
Note for future: Snapcraft seems to be changing how it handles 
[desktop interfaces](https://forum.snapcraft.io/t/the-desktop-interfaces/2042).
See [this post](https://forum.snapcraft.io/t/desktop-app-support-gtk/6834). 

