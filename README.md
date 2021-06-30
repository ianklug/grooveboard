# Grooveboard
A four-key mechanical keyboard for rhythm games.

Design by [ianklug](https://ianklug.com). Art by [clue](https://clue.graphics). Made with KiCad 5.

Please clone this repository using the `--recurse-submodules` flag. Many of the required symbol and footprint libraries will not be included otherwise.

**UPDATE 2021-06-30: Alternate versions of Grooveboard MX and Grooveboard Choc have been added using the larger AU variant of the microcontroller. Due to parts availability, these are the designs that will be used for the upcoming limited production run of Grooveboard.**

**Please note that for now, the AU versions require different firmware to the original MU versions as the switches are wired to different pins. This will change soon, as the MU designs (which have not yet been manufactured) will be updated to use the same pin wiring as the AU versions.**

## Variations

**Grooveboard:** Compatible with MX, Choc, or Alps switches. Switches must be soldered.

**Grooveboard MX:** Compatible with MX switches only. Uses Kailh MX hot-swap sockets.

**Grooveboard Choc:** Compatible with Choc switches only. Uses Kailh Choc hot-swap sockets.

## Firmware

Grooveboard is powered by [QMK Firmware](https://qmk.fm). You can find the default .hex files in the `firmware` directory.

Precompiled firmwares are provided for the two versions of Grooveboard (AU and MU). Please choose the firmware for the version of grooveboard that you have - for the moment they are not cross-compatible.

If you are interested in dynamically modifying your keymap without reflashing your board, firmwares compatible with [VIA Configurator](https://caniusevia.com) have also been provided. As of now they are not available in VIA by default, but you can still use it.

In VIA's Settings, switch on "Show Design Tab." Then choose the new "Design" tab and click the large "Upload" button to add a draft definition for Grooveboard. This draft definition, `ianklug-grooveboard-via-definition.json`, can be found in the `firmware` directory. Once you have done this, the keyboard should be detected by VIA when plugged in, and you can change its keymap dynamically.

## Ordering

Zipped gerber files are present for each variation of Grooveboard. They are called `<variation>-gerbers-v1.zip`.

The least expensive way to obtain a Grooveboard for yourself if they are not currently on sale is likely from [JLCPCB](https://jlcpcb.com). However, they have a minimum order quantity of five boards.

If you will be ordering from JLCPCB, use `<variation>-gerbers-jlcpcb-v1.zip`, and make sure to choose "Specify a location" under "Remove Order Number".

For JLCPCB's SMT assembly service, select assembly for the bottom of the board. Use `<variation>-bom.csv` and `<variation>-bottom-pos.csv` for your BOM and Centroid files. Note that you will still need to obtain and solder the USB-C connector yourself, as well as either the hot-swap sockets or the switches themselves.

For the USB connector, use a [GCT USB4085](https://gct.co/connector/usb4085).

For the hot-swap sockets, use [Kailh sockets](https://www.kailhswitch.com/mechanical-keyboard-switches/box-switches/mechanical-keyboard-switches-kailh-pcb-socket.html). Please note that the sockets are different for MX switches and Choc switches!
