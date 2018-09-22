## Redox Wireless (a.k.a. codename Ultron)

The Redox Wireless is the wireless version of the Redox keyboard.

### Summary

  - [Bill of materials](#bill-of-materials)
  - [Transmitters Assembly](#transmitters-assembly)
  - [Firmware](#firmware)

#### Bill of materials

##### Transmitters

| Qty | Item                                          | Notes                                               |
|----:|-----------------------------------------------|-----------------------------------------------------|
|  70 | Cherry MX compatible switches                 |                                                     |
|   2 | Redox Wireless PCBs                           | [Availalble here]()                                 |
|   2 | YJ-14015 modules (Core51822B clones)          | [aliexpress](https://www.aliexpress.com/item/NRF51822-Core51822-BLE-4-0-Bluetooth-2-4G-Wireless-Module-Antenna-Board-For-ULP-SPI-I2C/32842154172.html?spm=2114.search0104.3.8.663a616aYeRlVr&ws_ab_test=searchweb0_0,searchweb201602_1_10065_10068_10843_10059_10884_10887_10696_100031_10084_10083_10103_10618_10304_10307_10820_10821_10302,searchweb201603_60,ppcSwitch_5&algo_expid=1dded059-5054-4890-bcc4-6face1150a21-1&algo_pvid=1dded059-5054-4890-bcc4-6face1150a21&priceBeautifyAB=0)
|  70 | 1N4148 diodes                                 | SMD diodes can also be used                         |
|   2 | Keystone 3034 SMT battery holders             | [digikey](https://www.digikey.com/product-detail/en/keystone-electronics/3034/36-3034-ND/4499289)|
|   2 | JS102011SAQN SMT slide switch                 | [digikey](https://www.digikey.com/product-detail/en/c-k/JS102011SAQN/401-1999-1-ND/1640114)|
|   2 | Right angle 0.1" header (1x4pin)              |                                                     |

##### Receiver

You can refer directly to the [Mitosis-hardware repository](https://github.com/reversebias/mitosis-hardware/blob/master/bom/README.md) since the recevier is exactly the same, or you can build a receiver on your own.

| Qty | Item                                          | Notes                                               |
|----:|-----------------------------------------------|-----------------------------------------------------|
|   1 | Receiver Interface PCB                        | [files](https://github.com/reversebias/mitosis-hardware/tree/master/gerbers)                                           |
|   1 | Core51822(B) or YJ-14015 modules              | [direct](http://www.waveshare.com/core51822-b.htm), [aliexpress](https://www.aliexpress.com/w/wholesale-core51822-b.html?initiative_id=SB_20170426175446&site=glo&groupsort=1&SortType=price_asc&g=y&SearchText=core51822+b)                          |
|   1 | Arduino Pro Micro compatible microcontroller  |                                                     |
|   1 | Cree CLVBA-FKA                                | [digikey](https://www.digikey.com/product-detail/en/cree-inc/CLVBA-FKA-CAEDH8BBB7A363/CLVBA-FKA-CAEDH8BBB7A363CT-ND/2650500)|
|   1 | 1117 3.3v regulator in SOT223                 | [digikey](https://www.digikey.com/product-detail/en/diodes-incorporated/AZ1117IH-3.3TRG1/AZ1117IH-3.3TRG1DICT-ND/5699682)|
|   2 | 1206 4.7k resistor array                      | [digikey](https://www.digikey.com/product-detail/en/stackpole-electronics-inc/RAVF164DJT4K70/RAVF164DJT4K70CT-ND/2425255)|
|   2 | SMD tactile button                            | [digikey](https://www.digikey.com/product-detail/en/c-k/PTS525SM15SMTR2-LFS/CKN9104CT-ND/1146923)|
|   1 | Right angle 0.1" header (1x4pin)              |                                                     |
|   2 | Straight 0.1" header (1x6pin)                 |                                                     |

#### Transmitters Assembly

WIP

#### Firmware

This keyboard uses two types of MCUs so it needs two different firmwares. For flashing the firmware use the following order:

1. Receiver
2. Pro Micro
3. Transmitters

##### Nordic MCUs Firmware

Follow the instruction in the [Redox Wireless Keyboard firmware repository](https://github.com/mattdibi/redox-w-firmware). You'll need only to flash the pre-built `.hex` files to the corresponding MCUs, for this you'll need an STLinkV2 debugger.

##### Arduino Pro Micro Firmware

The Redox uses QMK for its firmware, follow the QMK installation instructions [here](https://docs.qmk.fm/#/getting_started_build_tools), then compile and burn the firmware as follows:

```sh
$ cd path/to/qmk_firmware
$ make redox_w/rev1:default:avrdude
```

You can find the code for the Redox here: [QMK - Redox Wireless keyboard](https://github.com/mattdibi/qmk_firmware/tree/redox_wireless/keyboards/redox_w).

In the [Redox Wireless Keyboard firmware repository](https://github.com/mattdibi/redox-w-firmware/tree/master/precompiled) I added some pre-built hex files with the default keymap for testing purpose.

