# Grooveboard
A four-key mechanical keyboard for rhythm games.

![Grooveboard PCB](https://i.imgur.com/wbMkbHX.jpg)

Design by [ianklug](https://ianklug.com). Art by [clue](https://clue.graphics).

Special thanks to [Sebastiaan Swinkels](https://github.com/C44Supra) for technical assistance.

Made with [KiCad](https://www.kicad.org/).

*Please clone this repository using the `--recurse-submodules` flag. Some of the required symbol and footprint libraries will not be included otherwise.*

## Versions

*Please note that the RP2040 models are functional at a hardware level, but software is incomplete.*

The 2.x versions (grooveboard-rp) use the RP2040 MCU, and require different firmware from the 1.x versions. They also include a few new features and refinements over the 1.x models, including M2 mounting holes and improved key spacing.

The 1.x versions (grooveboard-atmel) use the Atmega32U4 MCU, in either the MU or AU footprint. These versions are no longer recommended.

There are three types of Grooveboard, each supporting different types of switches.

**Grooveboard:** Compatible with MX, Choc, or Alps-style switches. Switches must be soldered.

**Grooveboard MX:** Compatible with MX-style switches only. Uses Kailh MX hot-swap sockets.

**Grooveboard Choc:** Compatible with Choc-style switches only. Uses Kailh Choc hot-swap sockets.

## Firmware

Grooveboard is powered by [QMK Firmware](https://qmk.fm).

Grooveboard ships by default with firmware supporting [VIA Configurator](https://caniusevia.com). To modify your keymap, install VIA Configurator, plug in your Grooveboard, and begin customizing. Changes will be applied immediately.

For more advanced functionality, you may also customize Grooveboard using [QMK Configurator](https://config.qmk.fm), or by using QMK on the command line. This will require a reflash of your board's firmware. Use [QMK Toolbox](https://github.com/qmk/qmk_toolbox) to flash if on Windows or MacOS, or the QMK CLI with avrdude on Linux.

## Manufacturing

**Manufacture at your own risk. I can not guarantee the quality or functionality of boards not sold directly by me.**

**Please note that most PCB manufacturers have a minimum order quantity of five units.**

Hand-soldering Grooveboards from scratch is extremely difficult and NOT recommended due to the small size of the surface-mount components and their pads. Instead, PCB assembly services can source and assemble all the small parts on the bottom of the board. Depending on the manufacturer, you may only need to hand-solder some of the larger parts, such as the USB port and the switches/sockets.

I can personally recommend [JLCPCB](https://jlcpcb.com) or [PCBWay](https://pcbway.com/), but most PCB manufacturers should be capable of producing Grooveboard.

Zipped gerber files are present for the production designs of each variation of Grooveboard. They are called `<variation>-gerbers-<version>.zip` and should be compatible with most PCB manufacturing services.

If you will be ordering from JLCPCB, use `<variation>-gerbers-jlcpcb-<version>.zip`. These gerbers have the JLCPCB serial number placed in an easily-readable location on the back of the board. Make sure to choose "Specify a location" under "Remove Order Number" so that this number is printed where expected.

Production Grooveboards are two-layer FR4, 1.6mm thick. The RP2040 versions measure 120x25mm. They are assembled using lead-free solder. BOM and Centroid files are present for each board in the format expected by JLCPCB.

The USB connector is a [GCT USB4085](https://gct.co/connector/usb4085). The hot-swap sockets are [Kailh sockets](https://www.kailhswitch.com/mechanical-keyboard-switches/box-switches/mechanical-keyboard-switches-kailh-pcb-socket.html). **Sockets are different for MX switches and Choc switches! Make sure to use the right kind for the model you have chosen.**

## License

Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
