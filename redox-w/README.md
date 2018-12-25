## Redox Wireless (a.k.a. codename Ultron)

The Redox Wireless is the wireless version of the Redox keyboard.

### Summary

  - [Bill of materials](#bill-of-materials)
  - [Transmitters Assembly](#transmitters-assembly)
  - [Receiver Assembly](#receiver-assembly)
  - [Firmware](#firmware)

#### Bill of materials

##### Transmitters

| Qty | Item                                          | Notes                                               |
|----:|-----------------------------------------------|-----------------------------------------------------|
|  70 | Cherry MX compatible switches                 |                                                     |
|   2 | Redox Wireless PCBs                           |                                                     |
|   2 | YJ-14015 modules (Core51822B clones)          | [aliexpress](https://www.aliexpress.com/item/NRF51822-Core51822-BLE-4-0-Bluetooth-2-4G-Wireless-Module-Antenna-Board-For-ULP-SPI-I2C/32842154172.html?spm=2114.search0104.3.8.663a616aYeRlVr&ws_ab_test=searchweb0_0,searchweb201602_1_10065_10068_10843_10059_10884_10887_10696_100031_10084_10083_10103_10618_10304_10307_10820_10821_10302,searchweb201603_60,ppcSwitch_5&algo_expid=1dded059-5054-4890-bcc4-6face1150a21-1&algo_pvid=1dded059-5054-4890-bcc4-6face1150a21&priceBeautifyAB=0)
|  70 | 1N4148 diodes                                 | SMD diodes can also be used                         |
|   2 | Keystone 3034 SMT battery holders             | [digikey](https://www.digikey.com/product-detail/en/keystone-electronics/3034/36-3034-ND/4499289)|
|   2 | JS102011SAQN SMT slide switch                 | [digikey](https://www.digikey.com/product-detail/en/c-k/JS102011SAQN/401-1999-1-ND/1640114)|
|   2 | Right angle 0.1" header (1x4pin)              |                                                     |

##### Receiver

| Qty | Item                                          | Notes                                               |
|----:|-----------------------------------------------|-----------------------------------------------------|
|   1 | Redox receiver PCB                            |                                                     |
|   1 | YJ-14015 module (Core51822B clone)            | [direct](http://www.waveshare.com/core51822-b.htm), [aliexpress](https://www.aliexpress.com/w/wholesale-core51822-b.html?initiative_id=SB_20170426175446&site=glo&groupsort=1&SortType=price_asc&g=y&SearchText=core51822+b)                          |
|   1 | Arduino Pro Micro compatible microcontroller  |                                                     |
|   1 | 1117 3.3v regulator in SOT223                 | [digikey](https://www.digikey.com/product-detail/en/diodes-incorporated/AZ1117IH-3.3TRG1/AZ1117IH-3.3TRG1DICT-ND/5699682)|
|   7 | 0805(2012 metric) SMD resistors               | Values depends on usage, see below                  |
|   4 | 0805(2012 metric) SMD standard LEDs           |                                                     |
|   1 | Through hole momentary switch                 | Dimensions 6mm x 6mm x 4.3mm                        |
|   1 | Right angle 0.1" header (1x4pin)              |                                                     |
|   2 | Straight 0.1" header (1x6pin)                 |                                                     |

###### Resistor values

WIP

> :information_source: You can also use the [Mitosis receiver](https://github.com/reversebias/mitosis-hardware/blob/master/bom/README.md) since it's almost identical, or you can build a receiver on your own. 

> :warning: To program the YJ-14015 MCUs you need an ST-Link v2 programmer, these can be found on eBay or Aliexpress for as little as 2$ shipped. See [picture below](#nordic-mcus-firmware).

#### Transmitters Assembly

<p align="center">
<img src="../img/redox-w-pcb1.jpg" alt="Wireless redox PCBs" width="600"/>
</p>

Assembly steps:

- Solder components to PCBs (you can proceed in no particular order):
  1. Solder the YJ-14015.
  2. Solder 1N4148 diodes.
  3. Solder slider switches.
  4. Solder the battery holders. *Note*: Some solder is needed on the ground pad to contact properly with the battery. See [picture below](#battery-holder-installation-detail).
  5. Solder the programming headers.
- Fit the PCBs inside their cases.
- Add the switches to the plate.
- Solder switches to the PCB.
- Add the CR2032 batteries.
- Program the MCUs.
- Close the case.

##### Programming headers detail:

<p align="center">
<img src="../img/pcb-w-assembly2.jpg" alt="Programming headers detail" width="600"/>
</p>

##### MCUs detail:

<p align="center">
<img src="../img/pcb-w-assembly3.jpg" alt="MCUs detail" width="600"/>
</p>

##### Slider switch detail:

<p align="center">
<img src="../img/pcb-w-assembly4.jpg" alt="Slider switch detail" width="600"/>
</p>

##### Diodes installation detail:

<p align="center">
<img src="../img/pcb-w-assembly5.jpg" alt="Diode installation detail" width="600"/>
</p>

##### Battery holder installation detail:

<p align="center">
<img src="../img/battery-installation1.jpg" alt="Battery holder installation detail. Ground pad." width="300"/>
<img src="../img/battery-installation2.jpg" alt="Battery holder installation detail. Assembled." width="300"/>
</p>

##### Left and right hand completed assembly:

<p align="center">
<img src="../img/pcb-w-assembly6.jpg" alt="Left and right hand completed assembly" width="600"/>
</p>

##### Assembled PCB:

<p align="center">
<img src="../img/pcb-w-assembly1.jpg" alt="Wireless Redox assembled PCB" width="600"/>
</p>

#### Receiver Assembly

The assembly is streightforward, I suggest you to follow the following order:

1. Solder all the Mitosis receiver components on the PCB. Leave the programming header for last.
2. Solder the Arduino Pro Micro to the Mitosis receiver PCB.

> :warning: Notice the orientation of the RGB LED (Cree CLVBA-FKA). Here I highlighted the dot on the PCB which must match with the notch on the LED packaging.

<p align="center">
<img src="../img/redox-w-receiver-assembly-1.jpg" alt="Mitosis receiver PCB LED installation detail." width="300"/>
<img src="../img/redox-w-receiver-assembly-2.jpg" alt="RGB LED detail" width="300"/>
</p>

##### Assembled receiver PCB:

<p align="center">
<img src="../img/redox-w-receiver-assembly-3.jpg" alt="Receiver PCB assembly front." width="300"/>
<img src="../img/redox-w-receiver-assembly-4.jpg" alt="Receiver PCB assembly back." width="300"/>
</p>

*Notes*: 
- You might notice that I didn't soldered the second push button, this is because it's not used in the receiver firmware.
- I also didn't solder all the MCUs pins because not all are used and it was hard to solder.
- I used a YJ-14015 instead of a Core51822B module because I happen to have that one laying around. Using an actual Core51822B module makes the soldering much easier.
- Here I used female header pins to connect the Arduino to the receiver PCB, if you want a more compact solution solder the Arduino directly to the receiver.

##### Assembled receiver:

<p align="center">
<img src="../img/redox-w-receiver-assembly-5.jpg" alt="Receiver PCB assembly front." width="600"/>
</p>

#### Firmware

This keyboard uses two types of MCUs so it needs two different firmwares. For flashing the firmware use the following order:

1. Receiver
2. Pro Micro
3. Transmitters

##### Nordic MCUs Firmware

Follow the instruction in the [Redox Wireless Keyboard firmware repository](https://github.com/mattdibi/redox-w-firmware). You'll need only to flash the pre-built `.hex` files to the corresponding MCUs, for this you'll need an STLinkV2 debugger.

<p align="center">
<img src="../img/st-link-v2-programmer.jpg" alt="ST-Link v2 programmer" width="300"/>
</p>

##### Arduino Pro Micro Firmware

The Redox uses QMK for its firmware, follow the QMK installation instructions [here](https://docs.qmk.fm/#/getting_started_build_tools), then compile and burn the firmware as follows:

```sh
$ cd path/to/qmk_firmware
$ make redox_w/rev1:default:avrdude
```

You can find the code for the Redox here: [QMK - Redox Wireless keyboard](https://github.com/mattdibi/qmk_firmware/tree/redox_wireless/keyboards/redox_w).

In the [Redox Wireless Keyboard firmware repository](https://github.com/mattdibi/redox-w-firmware/tree/master/precompiled) I added some pre-built hex files with the default keymap for testing purpose.

