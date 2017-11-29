# Ergo42

**The Answer to the Ultimate Question of Life, the Universe, and at least Keyboards.**

7x4 ortho linear split keyboard.

![Ergo42](https://raw.githubusercontent.com/Biacco42/Ergo42/readme/readme_image/ergo42_image.jpg)

# Parts

- **2** PCB
- **2** 5V/16MHz Pro Micro compatible boards
- **56** 1N4148 diodes
- **2** [MJ-4PP-9 TRRS jacks](http://akizukidenshi.com/catalog/g/gC-06070/)
- **2** Case plate set
- **10** 10mm M3 standoffs
- **20** 6mm M3 screws
- **56** [Switches of your choice](https://mechanicalkeyboards.com/shop/index.php?l=product_list&c=107)
- **1** TRRS cable

**/!\** The M3 screws linked above may have a slight clearance issue with the keycap. You can countersink the head or use a screw with a lower profile head. I'm testing out button head screws to see if they work better.

## Mount the Diodes

Place the PCB as TRRS jacks on the inside, closest to one another.

- The **left PCB** will have the **TRRS jack on the right**
- The **right PCB** will have the **TRRS jack on the left**

Solder diodes on which side is depending on your switch plate's thickness. 3 mm thick acrylic plate may have diodes on any side. 5 mm one **should have diodes on the other side of switches**. 

> *Tip:* Only the side which opposites from switches is verified.

**Double check your work**. Black lines should be facing the square pad.

![diodes_01](https://raw.githubusercontent.com/Biacco42/Ergo42/readme/readme_image/pwjP0e8.jpg)

## Mount the TRRS Jack

Mount the TRRS jack on the side opposite from your switches. It should be on the bottom.

## Mount Header Pins

Solder **header pins** for Pro Micro. **DO NOT solder the Pro Micro at this time**

## Mount switches

Mount switches on the acrylic plate, set PCB to fit and solder switches. Nothing is difficult.

## Mount the Pro Micro

Ergo42's PCB is symmetrical but Pro Micro mount is different between left and right PCB.

- On the **left PCB** the Pro Micro's component side should be **face to PCB**
- On the **right PCB** the Pro Micro's component side should be **back to PCB**

![left side PCB](https://raw.githubusercontent.com/Biacco42/Ergo42/readme/readme_image/IMG_20171118_203023508.jpg)

Pro Micro has no reset switch. You can solder tact switch between GND and RST pins here.

## Assemble the case

Tighten the screws with standoffs.
Some [vinyl pads](https://www.amazon.co.jp/gp/product/B00V5MQWGS/ref=oh_aui_detailpage_o00_s00?ie=UTF8&psc=1) may help the keyboard's stability.
Install your keycaps.

## Flash QMK Firmware

QMK firmware for Ergo42 now abilable on [this repo at ergo42 branch](https://github.com/Biacco42/qmk_firmware/tree/ergo42).
This document doesn't cover how to build QMK. Prease refer to [QMK documents](https://docs.qmk.fm/).

Conntect the keyboard by usb cable to PC and run

```
$ make ergo42/rev1:default:avrdude
```

will build and try to flash your firmware. Follow the instractions that require to reset the Pro Micro.

This process may require privileges.

## All have done

Just go.
