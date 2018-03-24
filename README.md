# The Redox keyboard repository

<p align="center">
<img src="img/redox-logo.png" alt="Redox logo" width="600"/>
</p>

The Redox keyboard is an open-source [QMK based](https://github.com/qmk/qmk_firmware) ergonomic split mechanical keyboard. This repository will be used to share information about the project and instruction on how to use and assembly the Redox keyboard.

## Redox rev.1

The Redox rev.1 is the first available version of the Redox keyboard. Hardware availability:
  - [Falbatech](https://falba.tech/)

### Building instructions

  - [Bill of materials](#Bill-of-Materials)
  - [Assembly](#Assembly)
  - [Firmware](#Firmware)
  - [Layout customization](#Layout)

#### Bill-of-Materials

  - **70**x Cherry MX compatible switches
  - **2**x Redox PCBs
  - **70**x 1N4148 diodes (SMD diodes can also be used)
  - **2**x PJ-320A 4 Poles 3.5mm TRRS Connector
  - **2**x 4.7k Ohm resistors (need to be soldered on one half only)
  - **2**x Through hole momentary switch 6mm x 6mm x 4.3mm
  - **2**x Arduino Pro Micro compatible microcontrollers 
  - **70**x Cherry MX compatible keycaps
    - **10**x 1.25u keycaps
    - **6**x 1.5u keycaps
    - **54**x 1u keycaps
  - **1**x TRRS cable
  - **1**x USB micro cable

#### Assembly

<p align="center">
<img src="img/redox-pcb2.jpg" alt="Redox PCBs" width="600"/>
</p>

Installation steps:

- Solder components:
  1. Solder 1N4148 diodes.
  2. Solder PJ-320A connectors.
  3. Solder momentary switches.
  4. Solder 4.7k Ohm resistors **on one half only**.
  5. Solder the Pro Micro header pins (**do not solder the Pro Micro controllers yet**).
- Flip the PCBs.
- Solder switches to the PCB.
- Flip the PCBs again.
- Solder Pro Micros to the header pins following the PCB labelling.

##### Right hand back side:
<p align="center">
<img src="img/pcb-assembly1.jpg" alt="Right hand back side" width="600"/>
</p>

##### Left hand back side:
<p align="center">
<img src="img/pcb-assembly2.jpg" alt="Left hand back side" width="600"/>
</p>

##### Diode installation detail:
<p align="center">
<img src="img/pcb-assembly3.jpg" alt="Diode installation detail" width="600"/>
</p>

#### Firmware

WIP...

#### Layout

WIP...
