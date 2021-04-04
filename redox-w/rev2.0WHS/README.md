## Redox rev 2.0WHS (Wireless)

The Redox rev 2.0WHS is the wireless hot-swappable version of the Redox keyboard.

## Summary

  - [Bill of materials](#bill-of-materials)
  - [Transmitters Assembly](#transmitters-assembly)
  - [Receiver Assembly](#receiver-assembly)
  - [3D printed case](#3d-printed-case)

## Bill of materials

#### Transmitters

| Qty | Item                                          | Notes                                               |
|----:|-----------------------------------------------|-----------------------------------------------------|
|  70 | Cherry MX compatible switches                 |                                                     |
|  70 | Kailh PCB sockets CPG151101S11                |                                                     |
|   2 | Redox Wireless 2.0WHS PCBs                    |                                                     |
|   2 | YJ-14015 modules (Core51822B clones)          | [aliexpress](https://www.aliexpress.com/item/NRF51822-Core51822-BLE-4-0-Bluetooth-2-4G-Wireless-Module-Antenna-Board-For-ULP-SPI-I2C/32842154172.html?spm=2114.search0104.3.8.663a616aYeRlVr&ws_ab_test=searchweb0_0,searchweb201602_1_10065_10068_10843_10059_10884_10887_10696_100031_10084_10083_10103_10618_10304_10307_10820_10821_10302,searchweb201603_60,ppcSwitch_5&algo_expid=1dded059-5054-4890-bcc4-6face1150a21-1&algo_pvid=1dded059-5054-4890-bcc4-6face1150a21&priceBeautifyAB=0)
|  70 | SOD-123 1N4148/1N4148W diodes                 | 1N4148 THT diodes can also be used                  |
|   2 | Keystone 3034 SMT battery holders             | [digikey](https://www.digikey.com/product-detail/en/keystone-electronics/3034/36-3034-ND/4499289)|
|   2 | JS102011SAQN SMT slide switch                 | [digikey](https://www.digikey.com/product-detail/en/c-k/JS102011SAQN/401-1999-1-ND/1640114)|
|   2 | Right angle 0.1" header (1x4pin)              |                                                     |

#### Receiver

| Qty | Item                                          | Notes                                               |
|----:|-----------------------------------------------|-----------------------------------------------------|
|   1 | Redox receiver PCB                            |                                                     |
|   1 | YJ-14015 module (Core51822B clone)            | [aliexpress](https://www.aliexpress.com/item/NRF51822-Core51822-BLE-4-0-Bluetooth-2-4G-Wireless-Module-Antenna-Board-For-ULP-SPI-I2C/32842154172.html?spm=2114.search0104.3.8.663a616aYeRlVr&ws_ab_test=searchweb0_0,searchweb201602_1_10065_10068_10843_10059_10884_10887_10696_100031_10084_10083_10103_10618_10304_10307_10820_10821_10302,searchweb201603_60,ppcSwitch_5&algo_expid=1dded059-5054-4890-bcc4-6face1150a21-1&algo_pvid=1dded059-5054-4890-bcc4-6face1150a21&priceBeautifyAB=0) |
|   1 | Arduino Pro Micro compatible microcontroller  |                                                     |
|   1 | 1117 3.3v regulator in SOT223                 | [digikey](https://www.digikey.com/product-detail/en/diodes-incorporated/AZ1117IH-3.3TRG1/AZ1117IH-3.3TRG1DICT-ND/5699682)|
|   2 | 330 Ohm 0805(2012 metric) SMD resistors       | Default configuration. Values depends on LED color, see [below](#resistor-values)|
|   2 | 220 Ohm 0805(2012 metric) SMD resistors       | Default configuration. Values depends on LED color, see [below](#resistor-values)|
|   3 | 1.5k Ohm 0805(2012 metric) SMD resistors      | Default configuration. See [below](#resistor-values)|
|   1 | Red 0805(2012 metric) SMD standard LED        | Default configuration.                              |
|   1 | Blue 0805(2012 metric) SMD standard LED       | Default configuration.                              |
|   1 | Green 0805(2012 metric) SMD standard LED      | Default configuration.                              |
|   1 | White 0805(2012 metric) SMD standard LED      | Default configuration.                              |
|   1 | Through hole momentary switch                 | Dimensions 6mm x 6mm x 4.3mm                        |
|   1 | Right angle 0.1" header (1x4pin)              |                                                     |
|   2 | Straight 0.1" header (1x6pin)                 |                                                     |

> :information_source: You can also use the [Mitosis receiver](https://github.com/reversebias/mitosis-hardware/blob/master/bom/README.md) since it's almost identical, or you can build a receiver on your own.

> :warning: To program the YJ-14015 MCUs you need an ST-Link v2 programmer, these can be found on eBay or Aliexpress for as little as 2$ shipped. See [picture below](#nordic-mcus-firmware).

##### Resistor values

If you want to customize your LEDs color or save a few bucks by ordering the LED all the same color you can refer to this section for choosing the correct resistor values. Otherwise you can refer to the [default configuration](#default-configuration).

There are two sets of resistor that you need for the receiver.

- The voltage divider resistors (`R1`, `R2` and `R3`): anything between 1.5k Ohm and 4.7k Ohm is good.
- The LEDs resistors (`R4`,`R6`,`R7` and `R8`): see the following table.

| LED color | Vf   | Suggested resistor value |
|-----------|------|--------------------------|
| Red       | 1.7V | 330 Ohm                  |
| Yellow    | 2.1V | 330 Ohm                  |
| Blue      | 3.2V | 220 Ohm                  |
| Green     | 2.2V | 330 Ohm                  |
| White     | 3.6V | 220 Ohm                  |

Depending on the color you choose to use you should use the resistor listed above.

#### Default configuration

Here you can find the default configuration for the receiver assembly.

| Label | Component         |
|-------|-------------------|
| D1    | Red LED           |
| D2    | Blue LED          |
| D3    | Green LED         |
| D4    | White LED         |
| R4    |  330 Ohm resistor |
| R6    |  220 Ohm resistor |
| R7    |  330 Ohm resistor |
| R8    |  220 Ohm resistor |
| R1    | 1.5k Ohm resistor |
| R2    | 1.5k Ohm resistor |
| R3    | 1.5k Ohm resistor |

## Transmitters Assembly

<p align="center">
<img src="../../img/redox-w-2.0-transmitters-assembly-1.jpg" alt="Redox 2.0WHS PCBs, unassembled." width="600"/>
</p>

Suggested assembly order (there's no wrong way of doing this because all parts can be soldered in any order):
1. Solder the YJ-14015.
2. Solder the right angle 0.1" header. To test the solder job try uploading the firmware as described in the dedicated section.
3. Solder the diodes taking into account the right orientation. You can now test if the PCB is working properly by connecting the STLinkV2 debugger for supplying power and using a pair of pliers to short the Kailh socket pins.
4. Solder the Kailh hot-swap sockets.
5. Solder the battery holders.
6. Solder the slide switch.

##### MCUs detail:

<p align="center">
<img src="../../img/redox-w-2.0-transmitters-assembly-2.jpg" alt="MCUs detail 1" width="300"/>
<img src="../../img/redox-w-2.0-transmitters-assembly-3.jpg" alt="MCUs detail 2" width="300"/>
</p>

##### Diodes and hot-swap socket detail:

<p align="center">
<img src="../../img/redox-w-2.0-transmitters-assembly-4.jpg" alt="Diode and hot-swap socket detail 1" width="300"/>
<img src="../../img/redox-w-2.0-transmitters-assembly-5.jpg" alt="Diode and hot-swap socket detail 2" width="300"/>
</p>

##### Assembled PCB:

<p align="center">
<img src="../../img/redox-w-2.0-transmitters-assembly-7.jpg" alt="Wireless Redox assembled PCB" width="600"/>
</p>

## Receiver Assembly

The receiver assembly is pretty straightforward, you can install the components in any order you like with the exception of the YJ-14015: it should be installed **after** the right angled header (PROGR_HEADER1). Suggested assembly order:

1. Solder D1, D2, D3 and D4 LEDs. See [image](#leds-installation-detail) for orientation.
2. Solder R4, R6, R7 and R8 resistors.
3. Solder R1, R2 and R3 resistors.
4. Solder the AMS1117.
5. Solder the Arduino Pro Micro headers.
6. Solder the programming headers. I suggest you to cut the excess of the header **before** soldering the headers. You should stay as flush to the PCB surface as possible since the controller will be soldered above the headers. Use some masking tape to help you keep the header in place while soldering.
7. Solder the YJ-14015. I suggest you to glue it in place or use some masking tape to help you during soldering.
8. Upload the firmware and you're done.

##### Assembled PCB, front:

<p align="center">
<img src="../../img/redox-w-receiver-assembly-1.jpg" alt="Assembled receiver PCB, front." width="600"/>
</p>

##### Assembled PCB, back:

<p align="center">
<img src="../../img/redox-w-receiver-assembly-2.jpg" alt="Assembled receiver PCB, back." width="600"/>
</p>

##### LEDs installation detail:

<p align="center">
<img src="../../img/redox-w-receiver-assembly-3.jpg" alt="Assembled receiver PCB, LEDs installation detail." width="600"/>
</p>

> :information_source: Please note that here I installed 220 Ohm resistors because I used only blue and white LEDs as I only had those laying around. You should use the resistor values suggested [here](#resistor-values) or follow the [default configuration](#default-configuration).

## 3D printed case

<p align="center">
<img src="../../img/redox-w-2.0-case-1.jpg" alt="3D printed case" width="600"/>
</p>

Here you can find the newly design minimal footprint case for the Redox 2.0 WHS. Features:
- Easy to print
- Sturdy feeling
- Minimal footprint
- Integrated sound dampening

I printed it with my Prusa Mini with 0.2 mm layer height. The STLs are for the left hand keyboard only, you'll need to mirror them along the X axis in your slicer for the right hand keyboard.

Hardware required for assembly:
- 10x M3 8 mm screws
- 10x M3 nuts

> :warning: The 3D printed case requires the use of SMD diodes. Through hole diodes will interfer witht the front plate.

> :warning: The closed back design (file: `BackplateL.stl`) was not tested at the time of this writing.

