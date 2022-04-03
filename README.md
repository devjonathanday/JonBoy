# JonBoy

## Overview
The JonBoy is a portable emulator with built-in peripherals, computer and battery. The shell is 3D printed, with the electronics mounted to the internal mounting holes. This repository contains various files needed to construct the device. Documentation for the components used, dimensions for the shell and hardware, and assembly instructions can be found in the Documentation folder, the original Blender models in the Blender folder, and the files used for printing in the STL folder.

### Disclaimer

Slight modification to the hardware is required for assembly. Generally, some parts of the hardware must be removed to accomplish a more compact form factor.

## Hardware

All hardware components used, along with links to purchase locations, are listed in the Specification document in the Documentation folder.

### Computer
The heart of the build is a Raspberry Pi 4, but it can easily accomodate a Raspberry Pi 3 by reconfiguring the wiring. Other microcomputers may be compatible, given the mounting holes are in the same location and the wiring setup is similar, but major differences in these factors may disqualify them from installation. Depending on the software used, different amounts of memory may be required, but at least 2GB of memory is recommended. A CPU heatsink is recommended to aid in cooling.

### Screen
The screen is a 5-inch display with a resolution of 800x480. It is connected to the computer via HDMI, with an appropriate video cable converter if required (HDMI→Micro HDMI for RPi4, no converter needed for RPi3). The product linked in the documentation is a touch-screen model, but the touch screen functionality is not utilized for this device. It also has a GPIO header for direct plug-and-play with the computer, but it is removed for clearance.

### Peripherals
There are 13 buttons in total that need to be mounted to the shell (4 face buttons, 4 directional buttons, 2 shoulders, START, SELECT, and HOME). The buttons are 11mm in diameter.

There are also 2 power buttons on the top of the case (one to connect the battery to the UPS, the other to connect the UPS to the computer). Both switches need to be toggled on for gameplay, while only the left needs to be toggled on for charging.

### Cooling
A single 300mm fan is mounted to the bottom half of the shell. This is placed underneath the computer near the heatsink on the CPU, and flows air outward.

### Battery + Charger
The device uses a 3.7V 5000mAh battery, that is charged with an Adafruit PowerBoost 1000C. The charging port is exposed on the outside of the shell. Increased ampere/hour batteries may be used with a modified battery mount, but the bottom half of the shell must be printed with this in mind.

### Mounting Hardware

| Component | Count | Usage | Notes |
| --- | ----------- | --- | --- |
| M3x5 Screws                     | 23 | Face and auxiliary buttons, external shell | These are commonly used for assembling desktop PCs. They notably have a washer build into the head.
| M2x9 Screws                     | 4  | Computer mount | These are the same screws used for Xbox One controllers.
| M2.5x16 Screws + Hex Nuts       | 4  | Fan mount | Screws are external, nuts are internal.
| M2.5x7.5 + Hex Nuts             | 4  | Screen mount | These are typically packaged with the display.
| 6/32 x 3/4" Screws + Hex Nuts   | 2  | Battery mount | Screws are external, nuts are internal.
| 6/32 x 1 3/4" Screws + Hex Nuts | 4  | Power buttons and shoulder buttons | Screws are external, nuts are internal.

### Storage

An SD card with at least 4GB capacity is required for use (more may be needed depending on how much data is downloaded to storage).

## Software

• The OS image used is [RetroPie](https://retropie.org.uk/download/), which provides nearly everything needed to run emulators and navigate the menus using the built-in peripherals.

• [Retrogame](https://learn.adafruit.com/retro-gaming-with-raspberry-pi/overview) is used to map the peripherals to inputs. A configuration file holds the information for mapping the GPIO ports to the inputs. Following the [installation guide](https://learn.adafruit.com/retro-gaming-with-raspberry-pi/adding-controls-software) and [configuration guide](https://learn.adafruit.com/retro-gaming-with-raspberry-pi/configuring-retrogame), the PiGRRL 2 preset provides most of the buttons used. It is worth noting that Retrogame converts physical inputs to keyboard, which is then read by the emulator software.