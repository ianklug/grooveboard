# Grooveboard
A four-key mechanical keyboard for rhythm games.

![Grooveboard Choc PCB](https://i.imgur.com/wbMkbHX.jpg)

Design by [ianklug](https://ianklug.com). Art by [clue](https://clue.graphics).

Made with KiCad 5.

*Please clone this repository using the `--recurse-submodules` flag. Many of the required symbol and footprint libraries will not be included otherwise.*

## Versions

**Grooveboard:** Compatible with MX, Choc, or Alps-style switches. Switches must be soldered.

**Grooveboard MX:** Compatible with MX-style switches only. Uses Kailh MX hot-swap sockets.

**Grooveboard Choc:** Compatible with Choc-style low-profile switches only. Uses Kailh Choc hot-swap sockets.

There are two variations of each version of Grooveboard - MU and AU. It is often difficult to find the smaller QFN variant (MU) of the Atmega32u4 processor that Grooveboard was initially designed with. For this reason, variations of each Grooveboard have been added based on the larger QFP variant (AU). Both types function identically and use the same firmware.

## Firmware

Grooveboard is powered by [QMK Firmware](https://qmk.fm).

Grooveboard ships by default with firmware supporting [VIA Configurator](https://caniusevia.com). To modify your keymap, just install VIA Configurator, plug in your Grooveboard, and begin customizing. Changes will be applied immediately.

For more advanced functionality, you may also customize Grooveboard using [QMK Configurator](https://config.qmk.fm), or by using QMK on the command line. However, this will require a reflash of your board's firmware. Use [QMK Toolbox](https://github.com/qmk/qmk_toolbox) to flash if on Windows or MacOS, or the QMK CLI with avrdude on Linux. Press the button on the back of the board to enter bootloader mode.

## Ordering

Grooveboards are sometimes available for direct purchase at [my web store](https://shop.ianklug.com/products/grooveboard). As of August 2021, they are actively being produced. For stock updates, subscribe to the newsletter available there.

If they are not currently on sale, or you have modified the design, you may wish to manufacture them yourself.

## Manufacturing

**Manufacture at your own risk. I can not guarantee the quality or functionality of boards not sold directly by me.**

**Please note that most PCB manufacturers have a minimum order quantity of five units.**

Hand-soldering Grooveboards from scratch is technically possible for the AU variants, but is extremely difficult and NOT recommended due to the small size of the surface-mount components and their pads. Instead, PCB assembly services can source and assemble all the small parts on the bottom of the board. Depending on the manufacturer, you may only need to hand-solder some of the larger parts, such as the USB port and the switches or switch sockets.

I can personally recommend [JLCPCB](https://jlcpcb.com) or [PCBWay](https://pcbway.com/), but most PCB manufacturers should be capable of producing Grooveboard.

Zipped gerber files are present for the production designs of each variation of Grooveboard. They are called `<variation>-gerbers-v1.zip` and should be compatible with most PCB manufacturing services.

If you will be ordering from JLCPCB, use `<variation>-gerbers-jlcpcb-v1.zip`. These gerbers have the JLCPCB serial number placed in an easily-readable location on the back of the board.

Production Grooveboards are two-layer 1.6mm FR4, and measure 118x23mm. Choose your quantity of boards and your preferred solder mask color. Make sure to choose "Specify a location" under "Remove Order Number" so that the order number is printed where expected. You can typically leave everything else at default.

Select assembly for the bottom of the board. No tooling holes are included in the gerbers, so select "Added by JLCPCB" under "Tooling Holes". On the next page, use `<variation>-bom.csv` and `<variation>-bottom-pos.csv` for your BOM and Centroid files. Before finalizing your order, please ensure that the parts shown in the diagram are placed correctly over their pads, and in the correct orientation.

For the USB connector, you should use a [GCT USB4085](https://gct.co/connector/usb4085). For the hot-swap sockets, use [Kailh sockets](https://www.kailhswitch.com/mechanical-keyboard-switches/box-switches/mechanical-keyboard-switches-kailh-pcb-socket.html). **Sockets are different for MX switches and Choc switches! Make sure to use the right kind for the model you have chosen.** You probably also want to add rubber or silicone feet to stabilize your Grooveboard and prevent it from slipping. The production models use four 6x2mm circular bumpers.
