# Grooveboard
A four-key mechanical keyboard for rhythm games.

![Grooveboard Choc PCB](https://i.imgur.com/wbMkbHX.jpg)

Design by [ianklug](https://ianklug.com). Art by [clue](https://clue.graphics).

Made with KiCad 5.

Please clone this repository using the `--recurse-submodules` flag. Many of the required symbol and footprint libraries will not be included otherwise.

## Variations

**Grooveboard:** Compatible with MX, Choc, or Alps switches. Switches must be soldered.

**Grooveboard MX:** Compatible with MX switches only. Uses Kailh MX hot-swap sockets.

**Grooveboard Choc:** Compatible with Choc low-profile switches only. Uses Kailh Choc hot-swap sockets.

**UPDATE (2021-06-30): There are now two versions of each variation of Grooveboard - MU and AU. Due to chip shortages, it is often difficult to find the smaller QFN variant (MU) of the Atmega32u4 processor that Grooveboard was initially designed with. For this reason, versions of each Grooveboard have been added based on the larger QFP variant (AU). The upcoming production run of Grooveboards will use the AU versions.**

## Firmware

Grooveboard is powered by [QMK Firmware](https://qmk.fm). You can find the default .hex file in the `firmware` directory. All versions of Grooveboard use the same default firmware.

To flash the firmware, follow the instructions on the [QMK Flashing Firmware page](https://docs.qmk.fm/#/newbs_flashing). You can put the keyboard into bootloader mode by pressing the button on the underside of the board.

If you are interested in dynamically changing your keymap without re-flashing your board, firmware compatible with [VIA Configurator](https://caniusevia.com) has also been provided. Grooveboard is not currently available in VIA by default, but you can still use it.

First, flash the keyboard with the VIA version of the firmware.

Next, In VIA's Settings, switch on "Show Design Tab."

Then, choose the new "Design" tab and click the large "Upload" button to add a draft definition for Grooveboard. This draft definition, `ianklug-grooveboard-via-definition.json`, can be found in the `firmware` directory.

Once you have done this, the keyboard should be detected by VIA, and you can change its keymap dynamically.

## Ordering

Zipped gerber files are present for each variation of Grooveboard. They are called `<variation>-gerbers-v1.zip`.

The least expensive way to obtain a Grooveboard for yourself if they are not currently on sale is likely from [JLCPCB](https://jlcpcb.com). However, they have a minimum order quantity of five boards.

If you will be ordering from JLCPCB, use `<variation>-gerbers-jlcpcb-v1.zip`, and make sure to choose "Specify a location" under "Remove Order Number".

For JLCPCB's SMT assembly service, select assembly for the bottom of the board. Use `<variation>-bom.csv` and `<variation>-bottom-pos.csv` for your BOM and Centroid files. Note that you will still need to obtain and solder the USB-C connector yourself, as well as either the hot-swap sockets or the switches themselves.

For the USB connector, use a [GCT USB4085](https://gct.co/connector/usb4085).

For the hot-swap sockets, use [Kailh sockets](https://www.kailhswitch.com/mechanical-keyboard-switches/box-switches/mechanical-keyboard-switches-kailh-pcb-socket.html). Please note that the sockets are different for MX switches and Choc switches!
