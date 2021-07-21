# Grooveboard
A four-key mechanical keyboard for rhythm games.

![Grooveboard Choc PCB](https://i.imgur.com/wbMkbHX.jpg)

Design by [ianklug](https://ianklug.com). Art by [clue](https://clue.graphics).

Made with KiCad 5.

Please clone this repository using the `--recurse-submodules` flag. Many of the required symbol and footprint libraries will not be included otherwise.

## Versions

**Grooveboard:** Compatible with MX, Choc, or Alps switches. Switches must be soldered.

**Grooveboard MX:** Compatible with MX switches only. Uses Kailh MX hot-swap sockets.

**Grooveboard Choc:** Compatible with Choc low-profile switches only. Uses Kailh Choc hot-swap sockets.

There are two variations of each version of Grooveboard - MU and AU. It is often difficult to find the smaller QFN variant (MU) of the Atmega32u4 processor that Grooveboard was initially designed with. For this reason, variations of each Grooveboard have been added based on the larger QFP variant (AU). Both work identically and use the same firmware.

## Firmware

Grooveboard is powered by [QMK Firmware](https://qmk.fm).

Grooveboard ships by default with firmware supporting [VIA Configurator](https://caniusevia.com). To customize your keymap, just download and install VIA Configurator, and plug in your keyboard.

For more advanced functionality, you may also customize using [QMK Configurator](https://config.qmk.fm). However, this will require a reflash of your board's firmware.

## Ordering

Grooveboards are occasionally in stock for direct purchase at [my web store](https://shop.ianklug.com/products/grooveboard). For stock updates, subscribe to the newsletter available there.

If they are not currently on sale, and the parts are in stock, the least expensive way to obtain a Grooveboard for yourself is likely from [JLCPCB](https://jlcpcb.com). However, they have a minimum order quantity of five boards.

**Manufacture at your own risk. I am not responsible for boards that are not sold by me.**

Zipped generic gerber files are present for each variation of Grooveboard. They are called `<variation>-gerbers-v1.zip`.

If you will be ordering from JLCPCB, use `<variation>-gerbers-jlcpcb-v1.zip`, and make sure to choose "Specify a location" under "Remove Order Number".

For JLCPCB's SMT assembly service, select assembly for the bottom of the board. Use `<variation>-bom.csv` and `<variation>-bottom-pos.csv` for your BOM and Centroid files. Note that you will still need to obtain and solder the USB-C connector yourself, as well as either the hot-swap sockets or the switches themselves.

For the USB connector, use a [GCT USB4085](https://gct.co/connector/usb4085).

For the hot-swap sockets, use [Kailh sockets](https://www.kailhswitch.com/mechanical-keyboard-switches/box-switches/mechanical-keyboard-switches-kailh-pcb-socket.html). Please note that the sockets are different for MX switches and Choc switches!
