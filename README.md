# JonBoy

## Overview
The JonBoy is a portable emulator with built-in peripherals, computer and battery. The shell is 3D printed, with the electronics mounted to the internal mounting holes. This repository contains various files needed to construct the device. Documentation for the components used, dimensions for the shell and hardware, and assembly instructions can be found in the Documentation folder, while the STL files used for 3D printing are placed in the Models folder.

### Disclaimer

Slight modification to the hardware is required for assembly. Generally, some parts of the hardware must be removed to accomplish a more compact form factor.

## Hardware

All hardware components used, along with links to purchase locations, are listed in the Specification document in the Documentation folder.

### Computer
The heart of the build is a Raspberry Pi 4, but it can easily accomodate a Raspberry Pi 3 by reconfiguring the wiring. Other microcomputers may be compatible, given the mounting holes are in the same location and the wiring setup is similar, but major differences in these factors may disqualify them from installation. Based on the software used, at least 2GB of memory is required.

### Screen
The screen is a 5-inch display with a resolution of 800x480. It is connected to the computer via HDMI, with an appropriate video cable converter if required (HDMI→Micro HDMI for RPi4, no converter needed for RPi3). The product linked in the documentation is a touch-screen model, but the touch screen functionality is not utilized for this device. It also has a GPIO header for direct plug-and-play with the computer, but it is removed for clearance.

### Peripherals
There are 12 buttons in total that need to be mounted to the shell (4 face buttons, 4 directional buttons, 2 shoulders and 2 auxiliary). The buttons are 11mm in diameter.

### Battery + Charger
The device uses a 3.7V 5000mAh battery, that is charged with an Adafruit PowerBoost 1000C. The charging port is exposed on the outside of the case via an extension cable.