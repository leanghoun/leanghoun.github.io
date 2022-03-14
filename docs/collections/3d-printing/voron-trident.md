---
layout: default
title: Voron Trident
parent: 3D Printing
grand_parent: Collections
permalink: /docs/collections/3d-printing/voron-trident/
nav_order: 1
---

# Voron Trident
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

- TOC
{:toc}

---

![Voron Trident](../../../../assets/images/voron-trident.jpg)

![Voron Trident](../../../../assets/images/voron-trident-toolhead.jpg)

![Voron Trident](../../../../assets/images/voron-trident-skirt-buttons.jpg)

### References
*   GitHub - [VoronDesign/Voron-Trident](https://github.com/VoronDesign/Voron-Trident)
*   GitHub - [Fysetc/Fysetc-Spider](https://github.com/FYSETC/FYSETC-SPIDER)
*   GitHub - [AndrewEllis93's Print Tuning Guide](https://github.com/AndrewEllis93/Print-Tuning-Guide)
*   [Voron Initial Startup](https://docs.vorondesign.com/build/startup/)
*   [Serial Request](https://www.reddit.com/r/voroncorexy/comments/sdhsjg/voron_trident_300mm_serial_request_le0n2959/)

### Bill of Materials & Supplies
*   [BOM & Costs](https://docs.google.com/spreadsheets/d/19nlv9ndFdrLKIFwBDWHhvT5E2p-6kONis_83c0GkSzI/edit?usp=sharing)
*   Main color: [MatterHackers Build Series Black](https://www.matterhackers.com/store/l/175mm-abs-filament-black-1-kg/sk/MWVCRU99)
*   Accent color: [KVP Graphite](https://www.villageplastics.com/product/abs/)
*   [OpenBuilds Slot Covers](https://openbuildspartstore.com/slot-cover-panel-holder/)

### Mods & Tweaks
*   [Funny Pack](https://github.com/thiagolocatelli/Voron/tree/master/Mods/funny_pack) - Based on the [Fanny Pack](https://github.com/oab1/VoronMods/tree/main/v2.2%20Recirculating%20Filter) which is in turn based on the [Nevermore](https://github.com/nevermore3d), this exhaust filter uses dual 5015 fans to circulate air through [activated carbon pellets](https://envirosupply.net/products/4mm-pellet-virgin-coal-activated-carbon-charcoal-for-vapor-filtration-1-lb-bag). I ended up needing to print smaller mesh inserts to prevent pellets from falling out of the basket.
*   [Panel Lockers](https://github.com/v6cl/My-Voron2.4-Customs/tree/main/Panel_Locker) - Print-in-place, works with 1mm-foam-lined side panels, and has good clamping force. Has two drawbacks; (1) one face of the model prints at an angle and catches light badly, and (2) you can't put two lockers on adjacent panels in the same location. Considering replacing them with [this design](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/richardjm/snap-latch-2020), that uses filament as a hinge, or [Yeri's Magnetic Clips](https://github.com/Yeriwyn/VoronUsers/tree/V1-and-V2-panels/printer_mods/yeri/V1_V2_Trident_Magnetic_Panels/STL/Trident/300).
*   [Sturdy Handles](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/jeoje/Sturdy_Handles) - They mount well and do not interfere with panel removal, but the extrusions have a tendency to rotate. Need to remember to periodically retighten the frame.
*   [6-pin MicroFit Skirt Insert](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/StvPtrsn/Parts_Jigs_and_Mods/Parts) + [Lock](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Jon/adxl345_skirt_keystone/STL) - Provides an interface for the ADXL345 cable to make Input Shaper calibration easier.
*   [StealthBurner Beta](https://github.com/VoronDesign/Voron-Afterburner/tree/sb-beta/STLs/Stealthburner) - Using a beta revision on top of the new ClockWork1 printed parts. And using Hartk's PCB cover to contain the wiring though I do not have a toolhead PCB.
*   [Eddie's LED Bar Clip](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/eddie/LED_Bar_Clip) - They're nice! Easy to print, clips directly to 2020 extrusions, and have baffles to shield light from eyes. I did not extend the LED mounts fully from front to back, and chose to leave some room. Just in case I need space to mount a camera in the future.
*   [Meteyou's GCode Buttons](https://github.com/VoronDesign/VoronUsers/tree/master/legacy_printers/printer_mods/meteyou/gcode_buttons) - This version of skirt buttons uses mechanical switches for satisfying tactility. I also embedded 2x3x4 LEDs into the switches for some backlighting, and did a filament swap for the button covers.
*  [Killw2k's LCD Display Tweak - Remaining Time](https://www.reddit.com/r/VORONDesign/comments/rv9oxn/lcd_status_screen_tweak/) - This config modification moves the progress bar to the 4th row to make room for remaining time and total time, neither of which are shown by default.

### Mods to Consider
*   GitHub - [Yeri's Magnetic Panels](https://github.com/Yeriwyn/VoronUsers/tree/V1-and-V2-panels/printer_mods/yeri/V1_V2_Trident_Magnetic_Panels/STL/Trident/300)
*   GitHub - [Slidr666's OV5648 Camera Mount](https://github.com/Slidr666/VoronUsers/tree/master/printer_mods/Slidr/PanzerObserver2.4)

### Slicer
*   GitHub - [AndrewEllis93's PIF Profile](https://github.com/AndrewEllis93/Ellis-PIF-Profile)
*   [SuperSlicer Bed Model](https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/SuperSlicer)
*   [My Bed Texture](../../../../assets/images/superslicer-bed-plain.png)
