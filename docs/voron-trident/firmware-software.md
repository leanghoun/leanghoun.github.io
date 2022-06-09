---
layout: default
title: Firmware & Software
parent: Voron Trident
permalink: /docs/voron-trident/slicer-stuff/
nav_order: 5
---

# Firmware & Software

## MainSail

## Klipper

Klipper installs to multiple electronics. The controller board, the Pi (twice if you use Linux MCU for Input Shaper), Klipper Expander, etc. All of them require flashing to install the first time, and some of them require flashing to install updates. [Discord@Drachenkatze wrote up a guide](https://docs.vorondesign.com/community/howto/drachenkatze/automating_klipper_mcu_updates.html) on creating an *update-all.sh* bash script to flash the Spider and Linux MCU from the terminal with one command. This does require having a microSD card in the controller board.

`bash klipper/update-all.sh`

Unfortunately, Klipper Expander still requires manually adding/removing a jumper to enter DFU mode for flashing.

## SuperSlicer

![SuperSlicer Bed Model + Texture](../../../../assets/images/superslicer-bed-model-texture.jpg)
*SuperSlicer Bed Model + Texture*
{: .fs-2 .text-grey-dk-000 }

* GitHub - [AndrewEllis93's PIF Profile](https://github.com/AndrewEllis93/Ellis-PIF-Profile)
* [SuperSlicer Bed Model](https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/SuperSlicer)
* [My Bed Texture](../../../../assets/images/superslicer-bed-plain.png)