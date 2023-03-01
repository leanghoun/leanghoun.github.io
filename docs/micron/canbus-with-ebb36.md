---
layout: default
title: CANbus with EBB36
parent: Micron
permalink: /docs/micron/can-bus/
nav_order: 4
---

# CANbus with EBB36 & CANbridge
{: .no_toc }

![EBB36 & CANbridge](../../../../assets/images/can-complete-2.jpg)
*EBB36 & CANbridge*
{: .fs-2 .text-grey-dk-000 }

#### Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## BOM

* EBB36 v1.2 - [BigTreeTech](https://www.aliexpress.us/item/3256804056968166.html)
* Igus Chainflex CF77-UL-D - [Igus](https://www.igus.com/product?artNr=CF77-UL-03-04-INI)

## References

* [Maz0r's Klipper/CANbus Guide](https://github.com/maz0r/klipper_canbus/blob/main/index.md)
* [Maz0r's CANboot Guide](https://github.com/maz0r/klipper_canbus/blob/main/controller/canboot.md)
* [PDF] [BigTreeTech EBB36 CAN v1.1 User Manual](https://github.com/bigtreetech/EBB/blob/master/EBB%20CAN%20V1.1%20(STM32G0B1)/EBB36%20CAN%20V1.1/BIGTREETECH%20EBB36%20CAN%20V1.1%20User%20Manual.pdf)
* [PDF] [How to Use CAN Toolhead Boards Connected Directly to Octopus](https://www.teamfdm.com/applications/core/interface/file/attachment.php?id=1931&key=30cd978c47e210495b7115baa783a66c)
* [Software] [STM32CubeProgramer](https://www.st.com/en/development-tools/stm32cubeprog.html#get-software)

![EBB36](../../../../assets/images/can-ebb36.jpg)
*EBB36*
{: .fs-2 .text-grey-dk-000 }

## Procedure

This is mostly a rehash of the steps found in the excellent PDF above, found on TeamFDM and attributed to TJM on Facebook, with my own notes and experience sprinkled in. Specifically, the guide focuses on how to get an EBB36/EBB42 to work directly with the CAN bridge port of an Octopus/Octopus Pro without an adaptor board like the U2C.

### Overview

1. Install CANboot on the Raspberry Pi.
1. Re-`make` firmwares for both the Octopus and EBB to be CANboot-compatible.
1. Set up Octopus to use CANbridge mode to EBB.
1. Set up EBB for CAN communication.
1. Find Octopus serial and flash Octopus with CANboot `serial` command.
1. Set up CAN network.
1. Find CAN UUID for both Octopus and EBB.
1. Flash EBB with CANboot `CAN` command.
1. Update printer.cfg with EBB pins.

### Notes

* All specific terminal commands and `make` instructions are laid out very clearly in the PDF. Copying/pasting through the steps, and paying attention to my hardware specifics, I was able to complete the entire process. In fact, the only trouble I ran into was reversing the wires on the CAN cable leading from the EBB to the CANbridge port. The diagram at the end of the PDF shows the orientation of the High/Low/Vin/GND wires in the EBB connector. My mistake was not mirroring the layout for the wires being connected. Luckily, I did not fry my EBB board.

* Here's the easiest way to get the new firmware files after `make`. Right after generating a new bin file, use this command to move the file to a Mainsail/Fluidd-reachable folder: `cp ~/klipper/out/klipper.bin ~/klipper_logs/`. Then just right click and download the bin from your browser.

* For EBB v1.1 boards, its a good idea to not power the heater pins while you are flashing. There's a bug where the heaters will turn on in DFU mode. This is fixed in v1.2 boards.

* Dedicated probes like inductive, BLTouch/3DTouch, etc. can use the dedicated probe pins on the EBB board, but Klicky probes should use an available endstop pin. The probe pins have a built-in resistor that will interfere with Klicky and cause mis-triggers.

## EBB36 Mount

KayosMaker already designed a set of EBB36 mounts for various toolheads and extruders, but they don't fit the newest revisions of the CAN board. I used his as a starting point, but added/moved/removed features to make it work with EBB36 v1.2.

![EBB36 Mount](../../../../assets/images/can-ebb36-mount.jpg)
*EBB36 Mount*
{: .fs-2 .text-grey-dk-000 }

![EBB36 Mounted](../../../../assets/images/can-ebb36-mounted.jpg)
*EBB36 Mounted*
{: .fs-2 .text-grey-dk-000 }

The wires extend further out from the rear than I hoped. To make sure they didn't get caught on anything, I extended the printed part that actuates the Y limit switch about 14mm to trigger further out. Unfortunately, with my new Y max of 106, there's a substantial loss of Y travel.

Here, you can see the original Y limit switch actuator:

![EBB36 Mounted Rear](../../../../assets/images/can-ebb36-mounted-rear.jpg)
*EBB36 Mounted Rear*
{: .fs-2 .text-grey-dk-000 }

And this is the extended one:

![Extended Y Actuator](../../../../assets/images/can-ebb36-extended-y-actuator.jpg)
*Extended Y Actuator*
{: .fs-2 .text-grey-dk-000 }

I can live with it for now. Just glad Micron is printing again!

![CAN Complete - 1](../../../../assets/images/can-complete-1.jpg)
*CAN Complete - 1*
{: .fs-2 .text-grey-dk-000 }