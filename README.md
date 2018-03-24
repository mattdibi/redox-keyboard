# The Redox project repository

<p align="center">
<img src="img/redox-logo.png" alt="Redox logo" width="600"/>
</p>

The Redox project is an open-source, [QMK (Quantum Mechanical Keyboard Firmware)](https://github.com/qmk/qmk_firmware) powered, ergonomic split mechanical keyboard. This repository will be used to share information about the project and instruction on how to use and assembly the Redox keyboard.

**Designer's bio**: [Mattia Dal Ben (aka u/TiaMaT102)](mailto:matthewdibi@gmail.com) obtained a master's degree in Engineering Electronics with a specialization in Computer Science at the University of Udine. Currently works as a Software Engineer in R&D department for a big IoT and Embedded Computers company. Mechanical keyboard enthusiast and maker, the Redox keyboard is the result of all of his passions.


## Related projects

- Redox prototype
  - [Redox prototype](https://www.thingiverse.com/thing:2704567): handwired 3D printed Redox prototype. Freely available.
  - [Tilted Redox case](https://www.thingiverse.com/thing:2767216): tilted case for the Redox prototype.
  - [couscous-kbd](https://github.com/CoenSchalkwijk/couscous-kbd): Redox inspired parametric OpenSCAD keyboard design.

## Redox rev.1

The Redox rev.1 is the first commercially available version of the Redox keyboard.

Hardware availability:
  - [Falbatech](https://falba.tech/)

### Building instructions

  - [Bill of materials](#Bill-of-Materials)
  - [Assembly](#Assembly)
  - [Firmware](#Firmware)
  - [Layout customization](#Layout)

#### Bill-of-Materials

| Qty | Item                                          | Notes                                               |
|----:|-----------------------------------------------|-----------------------------------------------------|
|  70 | Cherry MX compatible switches                 |                                                     |
|   2 | Redox PCBs                                    |                                                     |
|  70 | 1N4148 diodes                                 | SMD diodes can also be used                         |
|   2 | PJ-320A 4 poles 3.5 mm TRRS connectors        |                                                     |
|   2 | 4.7 kOhm resistors                            | Need to be soldered on one half only                |
|   2 | Through hole momentary switch                 | Dimensions 6mm x 6mm x 4.3mm                        |
|   2 | Arduino Pro Micro compatible microcontrollers |                                                     |
|   1 | TRRS cable                                    |                                                     |
|   1 | USB micro cable                               |                                                     |
|  70 | Cherry MX compatible keycaps                  | 10x 1.25u keycaps, 6x 1.5u keycaps, 54x 1u keycaps, |

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
