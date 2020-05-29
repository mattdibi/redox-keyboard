<p align="center">
<img src="img/redox-logo.png" alt="Redox logo" width="600"/>
<img src="img/qmk-badge-dark.png" alt="QMK" width="145"/>
</p>

<h3 align="center">The Redox project repository</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-success.svg)]() 
[![GitHub Issues](https://img.shields.io/github/issues/mattdibi/redox-keyboard.svg)](https://github.com/mattdibi/redox-keyboard/issues)
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/mattdibi/redox-keyboard.svg)](https://github.com/mattdibi/redox-keyboard/pulls)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](/LICENSE)

</div>

---

The Redox project is an open-source, [QMK (Quantum Mechanical Keyboard Firmware)](https://github.com/qmk/qmk_firmware) powered, ergonomic split mechanical keyboard. This repository will be used to share information about the project and instruction on how to use and assemble the Redox keyboard.

<p align="center">
<img src="img/redox-1.jpg" alt="Redox" width="600" style="border-radius:3%"/>
</p>

**Designer's bio**: [Mattia Dal Ben (aka u/TiaMaT102)](mailto:matthewdibi@gmail.com) obtained a master's degree in Electrical Engineering with a specialization in Computer Science at the University of Udine. Currently works as a Software Engineer in R&D department for a big IoT and Embedded Computers company. Mechanical keyboard enthusiast and maker, the Redox keyboard is the result of all of his passions.

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
- Wireless

## Related projects

- [**Redox handwire**](https://www.thingiverse.com/thing:2704567)
  - [Tilted Redox case](https://www.thingiverse.com/thing:2767216): tilted case for the Redox prototype by jschloer.
  - [couscous-kbd](https://gitlab.com/cschalkwijk/couscous-kbd): Redox-inspired parametric OpenSCAD keyboard design.
  - [Redox tenting kit](https://www.thingiverse.com/make:484843): modified base to support tenting, mini-USB for the interconnect, and a hole for microswitch for reset needed when uploading new firmware by [Lenbok](https://github.com/Lenbok).
  - [Iris-inspired Redox case](https://github.com/Lenbok/scad-redox-case): a case inspired both by the Redox rev1.0 and the Iris designed with OpenSCAD by [Lenbok](https://github.com/Lenbok).
  - [Redodactyl keyboard](https://www.reddit.com/r/MechanicalKeyboards/comments/9j5pw5/enter_the_redodactyl_first_build/): handwired 3D printed Dactyl-inspired Redox variant by u/darknao.
- [**Redox Manuform**](https://www.thingiverse.com/thing:3503380): full rework of the Redox case inspired by the Dactyl Manuform. Designed by [Fosk\_LL](https://www.thingiverse.com/Fosk_LL/about). 
- [**Redox rev1.0**](https://github.com/mattdibi/redox-keyboard/tree/master/redox)
	- [3D printable case](https://www.thingiverse.com/thing:2886662), freely available.
	- [Redox keyboard case (high profile)](https://www.thingiverse.com/thing:3825752), by [Michele Ferri](https://www.thingiverse.com/sako83/about).
	- [Travel-friendly Redox Keyboard case](https://www.thingiverse.com/thing:3607303), by [Fosk\_LL](https://www.thingiverse.com/Fosk_LL/about).
	- Rev1.0 PCBs: available at [Falbatech's store](https://falba.tech/product/redox-pcb-electrical-boards-set-of-2/)
	- Commercially available cases:
		- [Falbatech's bamboo cases with tilt kit](https://falba.tech/product/redox-standard-lift-bamboo-wood-case-with-oil-finish/)
		- [Falbatech's fullhand bamboo cases](https://falba.tech/product/redox-fullhand-bamboo-wood-case-with-oil-finish-ver-2/)
		- [Falbatech's PVC cases](https://falba.tech/product/redox-standard-pvc-white-case/)
- [**Redox Wireless (a.k.a. codename Ultron)**](https://github.com/mattdibi/redox-keyboard/tree/master/redox-w)
    - [Hackaday project build logs](https://hackaday.io/project/160610/logs)
    - [QMK firmware for Redox wireless](https://github.com/mattdibi/qmk_firmware/tree/redox_wireless)
    - [Nordic MCUs firmware for Redox wireless](https://github.com/mattdibi/redox-w-firmware)
    - [3D printed case](https://github.com/mattdibi/redox-keyboard/tree/master/redox-w/case), freely available.
    - Rev1.0W PCBs: available at [Falbatech's store](https://falba.tech/product/redox-wireless-pcb-electrical-boards-set-of-2/)
    - Commercially available cases:
        - [Falbatech's bamboo and aliminium cases](https://falba.tech/product/redox-wireless-standard-lift-bamboo-wood-case-with-oil-finish/)
		- [Falbatech's fullhand bamboo cases](https://falba.tech/product/redox-wireless-standard-lift-bamboo-wood-case-with-oil-finish-ver-1/)
		- [Falbatech's PVC cases](https://falba.tech/product/redox-wireless-standard-pvc-white-case/)

### Affiliations

In partnership with Falbatech you can now use the code "**mattdibi05**" on Falbatech's store for a 5% OFF special discount.

### Donations

If you've read this far and found something useful, please consider donating to help me maintain and further develop this project.

<p align="center">
<a href="https://www.paypal.me/MattiaDalBen"><img src="img/donate-button.jpeg" alt="Donate button" width=300/></a>
</p>
