# Neoredox rev 1.0

The Neoredox rev 1.0 is the first functional version of the Neoredox keyboard.



## Summary

  - [Bill of materials](#bill-of-materials)
  - [Firmware](#firmware)
  - [RGB Underglow](#rgb-underglow)

## Bill of materials

| Qty | Item                                          | Notes                                               |
|----:|-----------------------------------------------|-----------------------------------------------------|
|  70 | Cherry MX compatible switches                 |                                                     |
|  70 | Cherry MX hotswap sockets                     |                                                     |
|   2 | Neoredox PCBs                                 |                                                     |
|  70 | SOD-123 1N4148/1N4148W diodes                 |	1N4148 THT diodes can also be used                  |
|   2 | PJ-320A 4 poles 3.5 mm TRRS connectors        |                                                     |
|   2 | 4.7 kOhm resistors                            | Need to be soldered on one half only                |
|   2 | Through hole momentary switch                 | Dimensions 6mm x 6mm x 4.3mm                        |
|   2 | JS102011SAQN SMT slide switch	                | |
|   2 | Arduino Pro Micro compatible microcontrollers | Beware of the infamous Green Pro Micro, see note below. |
|   1 | TRRS cable                                    |                                                     |
|   1 | USB micro cable                               |                                                     |
|  70 | Cherry MX compatible keycaps                  | 10x 1.25u keycaps, 6x 1.5u keycaps, 54x 1u keycaps  |
|  *  | neopixel leds                                 | Optional RGB-underglow                              |



## Assembly guide

<p align="center">
<img src="../img/redox-pcb2.jpg" alt="Redox PCBs" width="600"/>
</p>

Installation steps:

- Solder components:
  1. Solder 1N4148 diodes. Keep the diode legs for the right hand controller installation.
  2. Solder PJ-320A connectors.
  3. Solder momentary switches.
  4. Solder 4.7k Ohm resistors **on one half only**. If you are going for the RGB-underglow ignore this step.
  5. Solder the Pro Micro header pins (**do not solder the Pro Micro controllers yet**). This step may differ depending on which case you're using. Refer to the following:
    * See 3D-Printed case [right hand controller installation detail](#3d-printed-case-assembly).
    * See Falbatech's [bamboo case](#falbatechs-bamboo-case-assembly).
    * See [socketed Pro Micro installation guide](#pro-micro-sockets).
  6. Optional see [RGB-underglow instructions](#rgb-underglow).
- Flip the PCBs.
- Solder switches to the PCB.
  * If you want hot swappable switches, see
    [the hot swappable switch instructions](#hot-swappable-switches).
- Flip the PCBs again.
- Solder Pro Micros to the header pins **following the PCB labeling**. The Pro Micro on the right half should be installed with the bottom facing the Redox PCB, the Pro Micro on the left half should be installed with the bottom facing away from the PCB. See [pictures](#left-hand-back-side-1) for details.

##### Right hand back side:
<p align="center">
<img src="../img/pcb-assembly1.jpg" alt="Right hand back side" width="600"/>
</p>

##### Left hand back side:
<p align="center">
<img src="../img/pcb-assembly2.jpg" alt="Left hand back side" width="600"/>
</p>

##### Diode installation detail:
<p align="center">
<img src="../img/pcb-assembly3.jpg" alt="Diode installation detail" width="600"/>
</p>



## Firmware

This keyboard uses ZMK for building, so follow the instructions for installing and building in https://zmk.dev/docs/development/setup

The build command using docker is:

Run the build container
```bash
cd zmk_config
docker run -it -w /home/zmk -v $(pwd):/home/zmk/zmk-config:rw --name zmk_build zmkfirmware/zmk-build-arm:3.2-branch bash
```
Then inside the container execute:
``` bash
git clone https://github.com/zmkfirmware/zmk.git
cd zmk
west init -l app/
west update
```
This takes a bit, after that exit the container
 
restart the container and then execute:
```bash
docker start -i zmk_build
cd /home/zmk/zmk/app
docker rm -f zmk_build
```

otherwise:
``` bash
cd zmk_config
export NEOREDOX_FOLDER=$(pwd) && echo $NEOREDOX_FOLDER 
west build -b nrfmicro_13 -- -DZMK_CONFIG=$(NEOREDOX_FOLDER)
```