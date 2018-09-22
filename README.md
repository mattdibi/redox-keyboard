# The Redox project repository

<p align="center">
<img src="img/redox-logo.png" alt="Redox logo" width="600"/>
<img src="img/qmk-badge-dark.png" alt="QMK" width="145"/>
</p>

The Redox project is an open-source, [QMK (Quantum Mechanical Keyboard Firmware)](https://github.com/qmk/qmk_firmware) powered, ergonomic split mechanical keyboard. This repository will be used to share information about the project and instruction on how to use and assembly the Redox keyboard.

<p align="center">
<img src="img/redox-1.jpg" alt="Redox" width="600"/>
</p>

**Designer's bio**: [Mattia Dal Ben (aka u/TiaMaT102)](mailto:matthewdibi@gmail.com) obtained a master's degree in Engineering Electronics with a specialization in Computer Science at the University of Udine. Currently works as a Software Engineer in R&D department for a big IoT and Embedded Computers company. Mechanical keyboard enthusiast and maker, the Redox keyboard is the result of all of his passions.

## Rationale

The Redox is a keyboard project designed with ergonomics in mind. It uses Cherry MX style mechanical switches laid out in a 7x5 columnar stagger layout with components that can easily be sourced. 

The design was heavily inspired by the [Ergodox keyboard](https://www.ergodox.io/), and its main goal is to reduce the size without sacrificing too many keys, hence the name **Re**duced Ergo**dox**. 

As an Ergodox user I couldn't ignore the few flaws of the original design and in a moment of arrogance I tried to fix them, thus the Redox features:
- Easier to reach thumb cluster.
- Additional easy-to-reach rotated 1.25u thumb key.
- Reduced size.
- Reduced costs (the Redox uses Arduino Pro Micro instead of the Teensy 2.0).
- Either half can be plugged in to the PC since each half can act as the master.
- Either half can work as a standalone keyboard to be used as a macropad/gaming keyboard.
- RGB backlighting support.
- 3D-printer friendly case.

## Related projects

- Redox handwire
  - [Redox handwire](https://www.thingiverse.com/thing:2704567): handwired 3D printed Redox prototype. Freely available.
  - [Tilted Redox case](https://www.thingiverse.com/thing:2767216): tilted case for the Redox prototype by jschloer.
  - [couscous-kbd](https://github.com/CoenSchalkwijk/couscous-kbd): Redox-inspired parametric OpenSCAD keyboard design.
  - [Redox tenting kit](https://www.thingiverse.com/make:484843): modified base to support tenting, mini-USB for the interconnect, and a hole for microswitch for reset needed when uploading new firmware by [Lenbok](https://github.com/Lenbok).
  - [Iris-inspired Redox case](https://github.com/Lenbok/scad-redox-case): a case inspired both by the Redox rev1.0 and the Iris designed with OpenSCAD by [Lenbok](https://github.com/Lenbok).
- [**Redox rev1.0**]()
	- [3D printed case](https://www.thingiverse.com/thing:2886662), freely available.
	- Rev1.0 PCBs: available at [Falbatech's store](https://falba.tech/product/redox-pcb-electrical-boards-set-of-2/)
	- Commercially available cases:
		- [Falbatech's bamboo cases with tilt kit](https://falba.tech/product/redox-standard-lift-bamboo-wood-case-with-oil-finish/)
		- [Falbatech's fullhand bamboo cases](https://falba.tech/product/redox-fullhand-bamboo-wood-case-with-oil-finish-ver-2/)
		- [Falbatech's PVC cases](https://falba.tech/product/redox-standard-pvc-white-case/)
- [**Redox Wireless (a.k.a. codename Ultron)**]() (WIP)
    - Build logs:
        - [Project log 1](https://hackaday.io/project/160610-redox-keyboard/log/151325-redox-codename-ultron-pt1)
        - [Project log 2](https://hackaday.io/project/160610-redox-keyboard/log/151460-redox-codename-ultron-pt2)
        - [Project log 3](https://hackaday.io/project/160610-redox-keyboard/log/151621-redox-codename-ultron-pt3)
        - [Project log 4](https://hackaday.io/project/160610-redox-keyboard/log/151692-redox-codename-ultron-pt4)
        - [Project log 5](https://hackaday.io/project/160610-redox-keyboard/log/152261-redox-codename-ultron-pt5)
        - [Project log 6](https://hackaday.io/project/160610-redox-keyboard/log/152873-redox-codename-ultron-pt6)
        - [Project log 7](https://hackaday.io/project/160610-redox-keyboard/log/153064-redox-codename-ultron-pt7)
    - [QMK firmware for Redox wireless](https://github.com/mattdibi/qmk_firmware/tree/redox_wireless)
    - [Nordic MCUs firmware for Redox wireless](https://github.com/mattdibi/redox-w-firmware)

### Donations

If you've read this far and found something useful, please consider donating to help me maintain and further develop this project.

<p align="center">
<a href="https://www.paypal.me/MattiaDalBen"><img src="img/donate-button.jpeg" alt="Donate button" width=300/></a>
</p>
