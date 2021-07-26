# Grooveboard
A four-key mechanical keyboard for rhythm games.

![Grooveboard Choc PCB](https://i.imgur.com/wbMkbHX.jpg)

Design by [ianklug](https://ianklug.com). Art by [clue](https://clue.graphics).

Made with KiCad 5.

Please clone this repository using the `--recurse-submodules` flag. Many of the required symbol and footprint libraries will not be included otherwise.

## Versions

**Grooveboard:** Compatible with MX, Choc, or Alps-style switches. Switches must be soldered.

**Grooveboard MX:** Compatible with MX-style switches only. Uses Kailh MX hot-swap sockets.

**Grooveboard Choc:** Compatible with Choc-style low-profile switches only. Uses Kailh Choc hot-swap sockets.

There are two variations of each version of Grooveboard - MU and AU. It is often difficult to find the smaller QFN variant (MU) of the Atmega32u4 processor that Grooveboard was initially designed with. For this reason, variations of each Grooveboard have been added based on the larger QFP variant (AU). Both types work identically and use the same firmware.

## Firmware

Grooveboard is powered by [QMK Firmware](https://qmk.fm).

Grooveboard ships by default with firmware supporting [VIA Configurator](https://caniusevia.com). To customize your keymap, just download and install VIA Configurator, and plug in your keyboard.

For more advanced functionality, you may also customize using [QMK Configurator](https://config.qmk.fm), or by using QMK on the command line. However, this will require a reflash of your board's firmware. Use [QMK Toolbox](https://github.com/qmk/qmk_toolbox) to flash if on Windows or MacOS, and the QMK command line/avrdude on Linux. Press the button on the back of the board to enter bootloader mode.

## Ordering

Grooveboards are sometimes in stock for direct purchase at [my web store](https://shop.ianklug.com/products/grooveboard). For stock updates, subscribe to the newsletter available there. As of July 2021, they are actively being produced, but due to supply chain issues we do not currently wish to share availability timelines until boards are about to be in stock and ready to ship.

If they are not currently on sale, and the parts are in stock, you can manufacture them yourself.

The least expensive way to obtain your own Grooveboards is likely from [JLCPCB](https://jlcpcb.com). For a little more, I can also personally recommend [PCBWay](https://pcbway.com/). **Please note that most manufacturers have a minimum order quantity of five boards.**

**Manufacture at your own risk. I am not responsible for boards that are not sold by me.**

Zipped gerber files are present for each variation of Grooveboard. They are called `<variation>-gerbers-v1.zip` and should be compatible with nearly all PCB manufacturing services.

If you will be ordering from JLCPCB, use `<variation>-gerbers-jlcpcb-v1.zip`. These gerbers have the serial number placed in an easily-readable location on the back of the board.

Production Grooveboards are two-layer FR4, 1.6mm thick, 118x23mm. Choose your quantity of boards and your preferred solder mask color. Make sure to choose "Specify a location" under "Remove Order Number" so that the order number is printed where expected. You can typically leave everything else at default.

Attempting to hand-solder Grooveboards from scratch is only possible for the AU variant, and is NOT RECOMMENDED due to the small size of the surface-mount components and their pads. PCB assembly services such as JLCPCB's will source and assemble all the small parts on the bottom of the board for you, so all you will need to solder yourself is the USB-C connector on the front, and the hot-swap sockets on the back (if building a hot-swap model). For the USB connector, use a [GCT USB4085](https://gct.co/connector/usb4085). For the hot-swap sockets, use [Kailh sockets](https://www.kailhswitch.com/mechanical-keyboard-switches/box-switches/mechanical-keyboard-switches-kailh-pcb-socket.html). **Sockets are different for MX switches and Choc switches! Make sure to order the right kind.**

If you will use JLCPCB's SMT assembly service, select assembly for the bottom of the board. No tooling holes are included in the gerbers, so select "Added by JLCPCB" under "Tooling Holes". On the next page, use `<variation>-bom.csv` and `<variation>-bottom-pos.csv` for your BOM and Centroid files. Before finalizing your order, please ensure that the parts shown in the diagram are placed correctly over their pads, and in the correct orientation.
