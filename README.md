# Grooveboard
A four-key mechanical keyboard for rhythm games.

Design by [ianklug](https://ianklug.com). Art by [clue](https://clue.graphics). Made with KiCad 5.

Please clone this repository using the `--recurse-submodules` flag. Many of the required symbol and footprint libraries will not be included otherwise.

**UPDATE 2021-06-29: Due to parts availability, alternate versions of Grooveboard MX and Grooveboard Choc have been added using the larger AU variant of the microcontroller. These are the designs that will be used for the upcoming limited production run of Grooveboard. Please note that the AU variants require different firmware to the original MU versions as the switches are wired to different MCU pins.**

## Variations

**Grooveboard:** Compatible with MX, Choc, or Alps switches. Switches must be soldered.

**Grooveboard MX:** Compatible with MX switches only. Uses Kailh MX hot-swap sockets.

**Grooveboard Choc:** Compatible with Choc switches only. Uses Kailh Choc hot-swap sockets.

## Firmware

The same firmware should work on all variations of Grooveboard.

Grooveboard is powered by [QMK Firmware](https://qmk.fm). You can find the default .hex file in the `firmware` directory.

## Ordering

**Due to global chip shortages, the final production designs for Grooveboard have NOT yet been fully tested. Manufacture at your own risk!**

Zipped gerber files are present for each variation of Grooveboard. They are called `<variation>-gerbers-v1.zip`.

The least expensive way to obtain a Grooveboard for yourself if they are not currently on sale is likely from [JLCPCB](https://jlcpcb.com). However, they have a minimum order quantity of five boards.

If you will be ordering from JLCPCB, use `<variation>-gerbers-jlcpcb-v1.zip`, and choose "Specify a location" under "Remove Order Number".

For JLCPCB's SMT assembly service, select assembly for the bottom of the board. Use `<variation>-bom.csv` and `<variation>-bottom-pos.csv` for your BOM and Centroid files. Note that you will still need to obtain and solder the USB-C connector yourself, as well as the hot-swap sockets or the switches themselves.

For the USB connector, use a [GCT USB4085](https://gct.co/connector/usb4085).

For the hot-swap sockets, use [Kailh sockets](https://www.kailhswitch.com/mechanical-keyboard-switches/box-switches/mechanical-keyboard-switches-kailh-pcb-socket.html). Please note that the sockets are different for MX switches and Choc switches!
