# Grooveboard
A four-key mechanical keyboard for rhythm games.

Design by [ianklug](https://ianklug.com). Art by [clue](https://clue.graphics). Made with KiCad 5.

## Variations

**Grooveboard:** Compatible with MX, Choc, or Alps switches. Switches must be soldered.

**Grooveboard MX:** Compatible with MX switches only. Uses Kailh MX hot-swap sockets.

**Grooveboard Choc:** Compatible with Choc switches only. Uses Kailh Choc hot-swap sockets.

## Firmware

The same firmware should work on all variations of Grooveboard.

Grooveboard is powered by QMK Firmware. You can find the default .hex file in the `firmware` directory.

## Ordering

Zipped gerber files are present for each variation of Grooveboard. They are called `<variation>-gerbers-<version>.zip`.

The least expensive way to obtain a Grooveboard for yourself is from [JLCPCB](https://jlcpcb.com). However, they have a minimum order quantity of five boards.

If you will be ordering from JLCPCB, use `<variation>-gerbers-jlcpcb-<version>.zip`, and make sure to choose "Specify a location" under "Remove Order Number".

If you will be using JLCPCB's SMT assembly service, use `<variation>-bom.csv` and `<variation>-bottom-pos.csv` for your BOM and Centroid files.

You will need to solder the USB-C connector yourself, as well as either the switches or the hot-swap sockets.

For the USB connector, use a [GCT USB4085](https://gct.co/connector/usb4085). 

For the hot-swap sockets, use [Kailh sockets](https://www.kailhswitch.com/mechanical-keyboard-switches/box-switches/mechanical-keyboard-switches-kailh-pcb-socket.html). Please note that the sockets are different for MX switches and Choc switches!
