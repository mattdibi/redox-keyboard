# Redox rev 1.0

The Redox rev 1.0 is the first commercially available version of the Redox keyboard.

Hardware availability:
  - [Falbatech](https://falba.tech/)

## Summary

  - [Bill of materials](#bill-of-materials)
  - [Other assembly guides](#other-assembly-guides)
  - [Assembly guide](#assembly-guide)
  - [Firmware](#firmware)
  - [Hot swappable mod](#hot-swappable-mod)
  - [RGB Underglow](#rgb-underglow)

## Bill of materials

| Qty | Item                                          | Notes                                               |
|----:|-----------------------------------------------|-----------------------------------------------------|
|  70 | Cherry MX compatible switches                 |                                                     |
|   2 | Redox PCBs                                    | [Available here](https://falba.tech/product/redox-pcb-electrical-boards-set-of-2/)|
|  70 | 1N4148 diodes                                 | SMD diodes can also be used                         |
|   2 | PJ-320A 4 poles 3.5 mm TRRS connectors        |                                                     |
|   2 | 4.7 kOhm resistors                            | Need to be soldered on one half only                |
|   2 | Through hole momentary switch                 | Dimensions 6mm x 6mm x 4.3mm                        |
|   2 | Arduino Pro Micro compatible microcontrollers | Beware of the infamous Green Pro Micro, see note below. |
|   1 | TRRS cable                                    |                                                     |
|   1 | USB micro cable                               |                                                     |
|  70 | Cherry MX compatible keycaps                  | 10x 1.25u keycaps, 6x 1.5u keycaps, 54x 1u keycaps  |
|  14 | WS2812/WS2812B leds                           | Optional RGB-underglow                              |


> :warning: Pay attention to the Pro Micro you use in this project. Online you can find the infamous **Green Pro Micros** which have the same pinout of the normal Pro Micro but use a different power circuitry. Being the Redox a split keyboard that relies on detecting which side is directly powered to find which side is the master, these clones are not suited for the task. A more detailed explanation [here](http://www.40percent.club/2017/09/green-pro-micro.html). Please note that they can come in different colors, not necessarily green.

> :warning: Before you start, flash the [Firmware](#firmware) to the ProMicros to make sure they are alright.

## Other assembly guides

External links to some other guides to building the Redox keyboard:

- ["*Build your own keyboard*"](https://medium.com/@costask/build-your-own-keyboard-5df65cb68839) by @costask.
- [Imgur build log](https://imgur.com/a/a6ck2Nc) (3D printed case).
- ["*First Homebrew Keyboard -redox Build Log-*"](https://x1.inkenkun.com/archives/6007) by [インケンch](https://www.youtube.com/channel/UCXJZdip7JmW74HQHCtfYzFw) (Japanese only)
- ["*Split Keyboard Build*"](https://kubami.com/articles/split-keyboard-build/) by Kuba Misiorny @kubami.
- [Wooden case build with hand tools](https://www.instructables.com/Redox-Keyboard-With-Wooden-Case/) by Cédric Bosdonnat

### Video guides

Two great video guides by [インケンch](https://www.youtube.com/channel/UCXJZdip7JmW74HQHCtfYzFw) (Japanese only).

<p align="center">
<a href="http://www.youtube.com/watch?v=EVRlU_eR9j4"><img src="http://img.youtube.com/vi/EVRlU_eR9j4/0.jpg" alt="Redox hardware assembly" width="300"/></a>
<a href="http://www.youtube.com/watch?v=jRIRdfIIa1Q"><img src="http://img.youtube.com/vi/jRIRdfIIa1Q/0.jpg" alt="Redox firmware" width="300"/></a>
</p>

Another great guide by [Antonio Raptors](https://www.youtube.com/channel/UCNYbiq6AH8AdYTKMokKaviQ) (Spanish only).

<p align="center">
<a href="https://www.youtube.com/watch?v=wRvfs1tUpZ4"><img src="http://img.youtube.com/vi/wRvfs1tUpZ4/0.jpg" alt="Como hacer un teclado mecánico para diseño / gaming - REDOX ESPAÑOL" width="300"/></a>
</p>

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

### 3D Printed case assembly

To lower the build costs I designed a 3D printable case which you can find in this repository or on [thingiverse](https://www.thingiverse.com/thing:2886662), feel free to modify it to best suit your needs.

<p align="center">
<img src="../img/3d-printed-case.jpg" alt="3D printed case" width=600 />
</p>

Parts:

| Qty | Item                                          | Notes                                               |
|----:|-----------------------------------------------|-----------------------------------------------------|
|   1 | Left top plate                                | [RedoxRev1TopLeft.STL](https://github.com/mattdibi/redox-keyboard/blob/master/redox/case/RedoxRev1TopLeft.STL)|
|   1 | Left bottom                                   | [RedoxRev1BottomLeft.STL](https://github.com/mattdibi/redox-keyboard/blob/master/redox/case/RedoxRev1BottomLeft.STL)|
|   1 | Right top plate                               | [RedoxRev1TopRight.STL](https://github.com/mattdibi/redox-keyboard/blob/master/redox/case/RedoxRev1TopRight.STL)|
|   1 | Right bottom                                  | [RedoxRev1BottomRight.STL](https://github.com/mattdibi/redox-keyboard/blob/master/redox/case/RedoxRev1BottomRight.STL)|
|  10 | M3 x 8mm (or 5mm) screws                      |                                                     |

For the Pro Micro installation on the right hand use the diodes legs leftover from previous steps as this will make the controller's USB port much closer to the PCB, this is needed for the USB connector to fit in the 3D printed case. If you're using Falbatech's bamboo case this is not needed and you can use standard header pins. Right hand controller installation detail:

1. Use a breadboard to keep the diode's legs from falling.
2. Solder the diode's legs in place. You want to have the Pro Micro as close to the Redox's PCB as possible.
3. Cut the excess.
4. Apply some electrical tape under the controller to prevent shorts.
5. Install your preferred switches (**remember: the controller installation is the last step**).
6. Solder the controllers in place.

<p align="center">
<img src="../img/right-hand-controller-detail1.jpg" alt="Right hand controller installation detail" width="300"/>
<img src="../img/right-hand-controller-detail2.jpg" alt="Right hand controller installation detail" width="300"/>
</p>

Here's some measurements of the Pro Micro installation:

<p align="center">
<img src="../img/right-hand-controller-detail3.jpg" alt="Right hand controller installation detail" width="400"/>
</p>

### Falbatech's bamboo case assembly

If you're using Falbatech's bamboo case the use of the diode's legs is not needed and you can use standard header pins

<p align="center">
<img src="../img/falbatech-case-assembly.jpg" alt="Falbatech's case assembly" width="600"/>
</p>

## Firmware

> :warning: If you have a Redox with RGB backlight installed you **MUST** use the serial connection. For details see [the RGB underglow firmware instructions.](#rgb-underglow)

The Redox uses QMK for its firmware, follow the QMK installation instructions [here](https://docs.qmk.fm/#/getting_started_build_tools), then compile and burn the firmware on both halves as follows:

```sh
$ cd path/to/qmk_firmware
$ make redox/rev1:default:avrdude
```

After issuing this command you should see the following output:

```sh
Detecting USB port, reset your controller now.....
```

Now you should reset the Pro Micros using the reset button as seen in the following picture:

<p align="center">
<img src="../img/reset-mcu.jpg" alt="Reset button" width="300"/>
</p>

> :warning: You always need to burn the firmware on **BOTH** halves of the keyboard.

> :warning: Failing to upload Redox Firmware on Linux. Please refer to [issue #8060](https://github.com/qmk/qmk_firmware/issues/8060) of QMK firmware.

You can find the code for the Redox here: [QMK - Redox keyboard](https://github.com/qmk/qmk_firmware/tree/master/keyboards/redox).

In the [firmware/](https://github.com/mattdibi/redox-keyboard/tree/master/redox/firmware) folder I added some pre-built hex files with the default keymap for testing purpose. You can upload the firmware binaries directly using the command below:

```sh
avrdude -p atmega32u4 -P $(COM_PORT) -c avr109 -U flash:w:redox_rev1_default.hex
```

### Setting EE_hands to use either hands as master
If you define `EE_HANDS` in your `config.h`, you will need to set the EEPROM for the left and right halves.

The EEPROM is used to store whether the half is left handed or right handed. This makes it so that the same firmware file will run on both hands instead of having to flash left and right handed versions of the firmware to each half. To flash the EEPROM file for the left half run:
```
$ cd path/to/qmk/folder
avrdude -p atmega32u4 -P $(COM_PORT) -c avr109 -U eeprom:w:"./quantum/split_common/eeprom-lefthand.eep"
// or the equivalent in dfu-programmer
```
and similarly for right half
```
avrdude -p atmega32u4 -P $(COM_PORT) -c avr109 -U eeprom:w:"./quantum/split_common/eeprom-righthand.eep"
// or the equivalent in dfu-programmer
```

> :warning: Replace `$(COM_PORT)` with the port of your device (e.g. `/dev/ttyACM0`)

After you have flashed the EEPROM, you then need to set `EE_HANDS` in `keyboard/redox/keymaps/default/config.h` like so:

```c++
// ...
/* Use I2C or Serial, not both */

// #define USE_SERIAL
#define USE_I2C

/* Select hand configuration */

// #define MASTER_LEFT
// #define MASTER_RIGHT
#define EE_HANDS

#undef RGBLED_NUM
#define RGBLIGHT_ANIMATIONS
// ...
```

Then rebuild the hex files and reflash.

Note that you need to program both halves, but you have the option of using different keymaps for each half. You could program the left half with a QWERTY layout and the right half with a Colemak layout using bootmagic's default layout option. Then if you connect the left half to a computer by USB the keyboard will use QWERTY and Colemak when the right half is connected.

## Hot swappable mod

With a few modifications to the original design, it is possible to make a
Redox with hot swappable switches and socketed Pro Micros. This was tested
with Falbatech's PCBs and PVC cases. The switch hotswap mod should work with
any case with a top plate that the switches snap into, with about a millimeter
of extra clearance between the top plate and the PCB, and another extra half
millimeter or so between the PCB and case bottom. If your (non-Falba) PCBs
have particularly small diameter thru-holes for switch pins, check the
Mill-Max 7305 spec sheet to ensure the receptacles will fit.

### Extended bill of materials

| Qty | Item                                          | Notes                                               |
|----:|-----------------------------------------------|-----------------------------------------------------|
|   1 | Peel-A-Way Sockets (82 pin strip)             | Available from [keeb.io](https://keeb.io/collections/frontpage/products/peel-a-way-sockets-for-pro-micros?variant=12972145344606)|
| 140 | Mill-Max 7305 Pin Receptacles                 | Available from [Digi-Key](https://www.digikey.com/product-detail/en/mill-max-manufacturing-corp/7305-0-15-15-47-27-10-0/ED1039-ND/1765737) or [Mouser](https://www.mouser.com/ProductDetail/Mill-Max/7305-0-15-15-47-27-10-0?qs=sGAEpiMZZMtzcnMBgC2bs4r8MywUouWab4lhjKyTlYM%3D)|
|   1 | Roll of Kapton tape                           |                                                     |

Some extra Mill-Max receptacles may come in handy, in case of soldering
mistakes or manufacturing defects.

### Pro Micro Sockets

<p align="center">
<img src="../img/hs-mod-peelaway-socket.jpg" alt="Pro Micro Peel-A-Way socket top detail" width="300"/>
<img src="../img/hs-mod-peelaway-solder.jpg" alt="Pro Micro Peel-A-Way socket solder detail" width="300"/>
</p>

Socketing your microcontrollers will allow you to swap out broken Pro Micros,
or swap any Pro Micro pin-compatible microcontroller (with, for example, USB-C)
into a finished build. Before you begin, you'll want to follow the
[standard assembly guide steps](#assembly-guide)
for soldering 1N4148 diodes, PJ-320A connectors,
momentary switches, and any resistors you'll be using. Remember to
**trim the legs off your diodes and keep them**, as we'll be using the legs to
make pins for each Pro Micro.

Installation steps, after initial soldering:

1. Using scissors or flush cutters, cut out two 12-pin strips of Peel-A-Way
   sockets.
2. With the bottom side of the PCB (the side with the diodes, momentary
   switch, and TRRS connector visible) facing up, place the cut Peel-A-Way
   socket strips into the thru-holes where the Pro Micro headers would
   usually go.
3. Temporarily fasten the Peel-A-Way sockets to the PCB with Kapton tape.
4. Flip over the PCB.
5. Solder the sockets into the thru-holes.
6. Install your switches. This step differs depending on whether you plan
   on making your switches hotswappable:
   * For fixed, non-hotswap switches, follow [the standard assembly guide](#assembly-guide).
   * Hotswap switch builds should follow [the hot swappable switch install guide](#hot-swappable-switches).
7. Flip and orient your Pro Micro so that its labels match the labels on your
   PCB, then cover the bottom of the Pro Micro in electrical or Kapton tape
   to prevent shorts.
8. Thread the least bent of your trimmed diode legs through the thru-holes
   in your Pro Micro and into the corresponding sockets on the PCB.
9. Keeping the Pro Micro as level as possible, solder the diode legs to the
   Pro Micro. It may help to keep a USB cable attached to the Pro Micro, to
   help ensure the port ends up in a usable orientation.
10. Trim the excess length of the diode legs off of the top of the Pro Micro.
11. Repeat these steps for the other half of your Redox.

### Hot Swappable Switches

> :warning: A few things to keep in mind:
> - Some switch pins (so far, Kailh Box Royals) may be slighly too wide to
>   fit the Mill-Max receptacle. When in doubt, try it with spare receptacles.
> - The only thing keeping the PCB attached to the top plate is the switches;
>   if you remove too many (more than half per side), the PCB will detach and
>   fall into the case. Try to swap only a few switches at once.

<p align="center">
<img src="../img/hs-mod-finished.jpg" alt="Finished Redox with hotswap switches" width=600 />
</p>

To build a Redox with hot swappable switches, follow these steps instead of
the switch installation instructions in the standard build guide. Soldering
Mill-Max receptacles is trickier than soldering bare switch pins; a small
iron tip, small diameter solder, and relatively low temperatures are
recommended.

1. Take each of your switches and push a Mill-Max receptacle fully onto each
   pin. One end of the receptacle has a small ring around it that makes it
   wider than the other end; the receptacle should be oriented so that the
   wide end is touching the switch housing (and will end up on the top,
   plate-facing side of the PCB in the assembled keyboard).
2. Snap switches into each of the four corners of your top plate, and two
   more into the mounting holes that will be directly above the Pro Micro
   in the assembled keyboard.
3. Flip over the top plate and install the PCB.
   - The receptacles might be a tight fit for the PCB thru-holes; if so,
     press the PCB into the switches to make sure the PCB is fully mounted
     and level.
4. Install the rest of the switches, starting from the outside edges of the
   plate and moving inward.
   - Initially, installing switches will likely shift the surrounding unsoldered
     switches and the PCB out of position, so pinch any jostled switches and
     the PCB back together as you go.
   - Be careful not to apply too much pressure to the stem of the switch, as
     this could damage it.
5. Solder your switches, starting from the corners then going from the outside
   edges to the inner switches in roughly the same order as the previous step.
   - Before soldering each switch, apply pressure to the top of the switch
     and the bottom of the PCB a final time to ensure the switch, plate, and
     PCB are all properly seated.
   - Apply heat to the pin receptacle and pad, then melt your solder onto
     the pad. You will want a "volcano" shaped solder joint which fully
     encircles the bottom of the receptacle, but doesn't fill its inner
     surface.
   - If you need to test that you haven't accidentally soldered a pin
     permanently into its receptacle by allowing solder to spill into the
     inner surface of the receptacle, you can try and temporarily remove
     the switch as you would during a hot swap. Use a switch puller to depress
     the tabs on the top and bottom of the switch (or the left and right for
     the flipped 1.5u key switches), and gently pull up on the switch until
     it is free of the keyboard. Note that if the switch and receptacles are
     still hot, it might take some extra effort to pull out the switch.
     Next, snap the switch back into its socket, and fix any unsoldered
     switches that were knocked out of place during this process.
6. Repeat these steps for the other side of the keyboard.

##### Installing Mill-Max receptacles onto switch pins:
<p align="center">
<img src="../img/hs-mod-millmax.jpg" alt="Mill-Max receptacle installation" width="600"/>
</p>

##### Pins, receptacles, and PCB in proper alignment:
<p align="center">
<img src="../img/hs-mod-pre-solder.jpg" alt="Proper alignment of receptacles, pins, and PCB" width="600"/>
</p>

##### Soldered hot swap receptacles:
<p align="center">
<img src="../img/hs-mod-soldered.jpg" alt="Soldered hot swap receptacles" width="600"/>
</p>

## RGB Underglow

> :warning: With this configuration:
> - You don't need to solder the 4.7k resistors since the I2C connection won't be used.
> - You can use only one hand as master.

Parts:
- [ ] WS2812/WS2812B LED strip
- [ ] 24 AWG (or smaller) stranded wire (white, red, black are good choices)

Data connection:

```
Led strip Headers -> DIN -> DO -> TRRS pad -> (TRRS to other side) -> TRRS pad -> DIN
```

### Assembly: LEFT hand as master (usually plugged in to the PC)
- On the LEFT hand:
  1. Solder the LED Strip headers as seen in the pictures below.
  2. Solder the DO Pin of the RGB strip to the TRRS pad as seen in the figures below.
- On the RIGHT hand:
  1. Solder VCC and GND of the RGB strip to the LED Strip headers.
  2. Solder the DIN Pin of the RGB strip to the TRRS pad as seen in the figures below.
- Flash the firmware with the serial and RGB Backlight options on, specifying the number of LEDs installed (see instruction [here](#rgb-underglow-firmware)).

##### Left hand back side:
<p align="center">
<img src="../img/rgb-underglow1.jpg" alt="RGB underglow left hand backside" width="600"/>
</p>

##### Right hand back side:

<p align="center">
<img src="../img/rgb-underglow2.jpg" alt="RGB underglow left hand backside" width="600"/>
</p>

### Assembly: RIGHT hand as master
- On the RIGHT hand:
  1. Solder the LED Strip headers to the RGB strip.
  2. Solder the DO Pin of the RGB strip to the TRRS pad.
- On the LEFT hand:
  1. Solder VCC and GND of the RGB strip to the LED Strip headers.
  2. Solder the DIN Pin of the RGB strip to the TRRS pad.

### RGB Underglow firmware

To enable RGB backlighting you need to modify the default firmware as follows:
- Use serial communication instead of I2C.
- Set the master hand.
- Set the number of LED you installed.

To do this, modify `qmk_firmware/keyboards/redox/keymaps/default/config.h` as follows:

```c++
// ...

/* You need to use the sarial communication since we
used a cable to carry the data signal for the LED strip */
#define USE_SERIAL

/* Select hand configuration: you need to use as master
the hand that drives the LED strip */
#define MASTER_LEFT
// #define MASTER_RIGHT

/* Put the total number of led used here */
#undef RGBLED_NUM
#define RGBLIGHT_ANIMATIONS
#define RGBLED_NUM 14
#define RGBLIGHT_HUE_STEP 8
#define RGBLIGHT_SAT_STEP 8
#define RGBLIGHT_VAL_STEP 8

// ...
```

Then compile and burn the firmware on both controllers:

```sh
$ cd path/to/qmk_firmware
$ make redox/rev1:default:avrdude
```

## Layout

<p align="center">
<img src="../img/redox-layout.png" alt="Redox rev1.0 layout"/>
</p>

[KLE Layout permalink](http://www.keyboard-layout-editor.com/##@_name=Redox&author=Mattia%20Dal%20Ben&switchMount=cherry&plate:false&pcb:false%3B&@_x:3.5%3B&=%23%0A3&_x:10.5%3B&=*%0A8%3B&@_y:-0.875&x:2.5%3B&=%2F@%0A2&_x:1%3B&=$%0A4&_x:8.5%3B&=%2F&%0A7&_x:1%3B&=(%0A9%3B&@_y:-0.875&x:5.5%3B&=%25%0A5&_x:6.5%3B&=%5E%0A6%3B&@_y:-0.875&x:0.25&a:5&w:1.25%3B&=%60%0A%0A%0A%0A%0A%0ALayer%202&_a:4%3B&=!%0A1&_x:14.5%3B&=)%0A0&_a:5&w:1.25%3B&=-%0A%0A%0A%0A%0A%0ALayer%202%3B&@_y:-0.625&x:6.5%3B&=Layer%201&_x:4.5%3B&=Layer%201%3B&@_y:-0.75&x:3.5&a:4%3B&=E&_x:10.5%3B&=I%3B&@_y:-0.875&x:2.5%3B&=W&_x:1%3B&=R&_x:8.5%3B&=U&_x:1%3B&=O%3B&@_y:-0.875&x:5.5%3B&=T&_x:6.5%3B&=Y%3B&@_y:-0.875&x:0.25&a:5&w:1.25%3B&=TAB&_a:4%3B&=Q&_x:14.5%3B&=P&_a:5&w:1.25%3B&=%2F=%3B&@_y:-0.625&x:6.5&a:7&h:1.5%3B&=%5B&_x:4.5&h:1.5%3B&=%5D%3B&@_y:-0.75&x:3.5&a:4%3B&=D&_x:10.5%3B&=K%3B&@_y:-0.875&x:2.5%3B&=S&_x:1&n:true%3B&=F&_x:8.5&n:true%3B&=J&_x:1%3B&=L%3B&@_y:-0.875&x:5.5%3B&=G&_x:6.5%3B&=H%3B&@_y:-0.875&x:0.25&a:5&w:1.25%3B&=ESC&_a:4%3B&=A&_x:14.5%3B&=%2F:%0A%2F%3B&_a:5&w:1.25%3B&='%3B&@_y:-0.375&x:3.5&a:4%3B&=C&_x:10.5%3B&=%3C%0A,%3B&@_y:-0.875&x:2.5%3B&=X&_x:1%3B&=V&_x:8.5%3B&=M&_x:1%3B&=%3E%0A.%3B&@_y:-0.875&x:5.5%3B&=B&_x:6.5%3B&=N%3B&@_y:-0.875&x:0.25&a:5&w:1.25%3B&=SHIFT&_a:4%3B&=Z&_x:14.5%3B&=%3F%0A%2F%2F&_a:5&w:1.25%3B&=SHIFT%3B&@_y:-0.375&x:3.5%3B&=*%0A%0A%0A%0A%0A%0AALT&_x:10.5%3B&=Left%3B&@_y:-0.875&x:2.5%3B&=-&_x:12.5%3B&=Down%3B&@_y:-0.75&x:0.5%3B&=GUI&=+&_x:14.5%3B&=Up&=Right%3B&@_r:15&y:-2.625&x:5.75&w:1.25%3B&=%5C%0A%0A%0A%0A%0A%0ACTRL%3B&@_r:30&rx:6.5&ry:4.25&y:-1%3B&=PgUp&=PgDn%3B&@_h:1.5%3B&=Back%0A%0A%0A%0A%0A%0Aspace&_h:1.5%3B&=Del%3B&@_r:-30&rx:13&y:-1&x:-2%3B&=Home&=End%3B&@_x:-2&h:1.5%3B&=Enter&_h:1.5%3B&=Space%3B&@_r:-15&rx:0&ry:0&y:7.75&x:11.75&w:1.25%3B&=ALT)
