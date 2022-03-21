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
*Voron Trident with StealthBurner and skirt buttons*
{: .fs-2 .text-grey-dk-000 }

![Voron Trident Toolhead](../../../../assets/images/voron-trident-toolhead.jpg)
*StealthBurner toolhead*
{: .fs-2 .text-grey-dk-000 }

![Voron Trident Skirt Buttons](../../../../assets/images/voron-trident-skirt-buttons.jpg)
*Skirt buttons*
{: .fs-2 .text-grey-dk-000 }

## i. References
* GitHub - [VoronDesign/Voron-Trident](https://github.com/VoronDesign/Voron-Trident)
* GitHub - [Fysetc/Fysetc-Spider](https://github.com/FYSETC/FYSETC-SPIDER)
* GitHub - [AndrewEllis93's Print Tuning Guide](https://github.com/AndrewEllis93/Print-Tuning-Guide)
* [Voron Docs](https://docs.vorondesign.com/)
  - [Voron Initial Startup](https://docs.vorondesign.com/build/startup/)
* [Klipper Docs](https://www.klipper3d.org/Overview.html)
  - [Input Shaper & Measuring Resonances](https://www.klipper3d.org/Measuring_Resonances.html) - It can be useful to see your resonance charts with the manual method, but trying to interpret the graphs can be a bit nebulous. For simplicity, just run `SHAPER_CALIBRATE` and let the ADXL345 measure the resonances automatically. Don't forget to `SAVE_CONFIG` to commit.
* [MainSail Docs](https://docs.mainsail.xyz/)
* [Moonraker Docs](https://moonraker.readthedocs.io/en/latest/)
  - [PolicyKit Permissions](https://moonraker.readthedocs.io/en/latest/installation/#policykit-permissions) - After updating Moonraker, if you see errors related to PolicyKit, try re-adding these permissions.
* [Serial Request](https://www.reddit.com/r/voroncorexy/comments/sdhsjg/voron_trident_300mm_serial_request_le0n2959/)

## ii. Bill of Materials & Supplies
* [BOM & Costs](https://docs.google.com/spreadsheets/d/19nlv9ndFdrLKIFwBDWHhvT5E2p-6kONis_83c0GkSzI/edit?usp=sharing)
* Main color: [MatterHackers Build Series Black](https://www.matterhackers.com/store/l/175mm-abs-filament-black-1-kg/sk/MWVCRU99)
* Accent color: [KVP Graphite](https://www.villageplastics.com/product/abs/)
* [OpenBuilds Slot Covers](https://openbuildspartstore.com/slot-cover-panel-holder/)


## iii. Mods & Tweaks

#### Quick Links
* [Funny Pack](funny-pack)
* [Panel Lockers](panel-lockers)
* [Sturdy Handles](sturdy-handles)
* [6-pin MicroFit Skirt Insert + Lock](6-pin-microfit-skirt-insert)
* [StealthBurner Beta](stealthburner-beta)
* [Eddie's LED Bar Clip](eddies-led-bar-clip)
* [Meteyou's GCode Buttons](meteyous-gcode-buttons)
* [Killw2k's LCD Display Tweak - Remaining Time](killw2ks-lcd-display-tweak---remaining-time)

### Funny Pack

The [Funny Pack](https://github.com/thiagolocatelli/Voron/tree/master/Mods/funny_pack) is based on the [Fanny Pack](https://github.com/oab1/VoronMods/tree/main/v2.2%20Recirculating%20Filter) which is in turn based on the [Nevermore](https://github.com/nevermore3d), this exhaust filter uses dual 5015 fans to circulate air through [activated carbon pellets](https://envirosupply.net/products/4mm-pellet-virgin-coal-activated-carbon-charcoal-for-vapor-filtration-1-lb-bag) ([alternative source](https://www.amazon.com/EnviroSupply-Premium-Bituminous-Activated-Charcoal/dp/B00XNXC70W)). I ended up needing to print mesh inserts to prevent pellets from falling out of the basket.

### Panel Lockers

These [Panel Lockers](https://github.com/v6cl/My-Voron2.4-Customs/tree/main/Panel_Locker) are print-in-place, work with 1mm-foam-lined side panels, and have good clamping force. Has two drawbacks; (1) one face of the model prints at an angle and catches light badly, and (2) you can't put two lockers on adjacent panels in the same location. Considering replacing them with [this design](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/richardjm/snap-latch-2020), that uses filament as a hinge, or [Yeri's Magnetic Clips](https://github.com/Yeriwyn/VoronUsers/tree/V1-and-V2-panels/printer_mods/yeri/V1_V2_Trident_Magnetic_Panels/STL/Trident/300).

### Sturdy Handles

[Sturdy Handles](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/jeoje/Sturdy_Handles) mount well and do not interfere with panel removal, but the extrusions have a tendency to rotate. Need to remember to periodically retighten the frame.

### 6-pin MicroFit Skirt Insert

Two sources for this modd; [6-pin MicroFit Skirt Insert](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/StvPtrsn/Parts_Jigs_and_Mods/Parts) and the [Lock](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Jon/adxl345_skirt_keystone/STL). Provides an interface for the ADXL345 cable to make Input Shaper calibration easier.

### StealthBurner Beta

Using [StealthBurner Beta](https://github.com/VoronDesign/Voron-Afterburner/tree/sb-beta/STLs/Stealthburner) on top of the new ClockWork1 printed front. And using Hartk's PCB cover to contain the wiring though I do not have a toolhead PCB.

### Eddie's LED Bar Clip

Everyone likes [Eddie's LED Bar Clip](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/eddie/LED_Bar_Clip). Easy to print, clips directly to 2020 extrusions, and have baffles to shield light from eyes. I did not extend the LED mounts fully from front to back, and chose to leave some room. Just in case I need space to mount a camera in the future. Check out [Steve Build's stream](https://www.youtube.com/watch?v=qTTLXU41Q0o&t=5188s) to see how to wire them together into one 4-pin dupont connector.

### Meteyou's GCode Buttons

I like [Meteyou's GCode Buttons](https://github.com/VoronDesign/VoronUsers/tree/master/legacy_printers/printer_mods/meteyou/gcode_buttons) because they use mechanical keyboard switches for satisfying tactility and are simple to light up with embedded 2x3x4 LEDs.

* *Preheat* - Cycles between "cooldown/white dial", "PLA temp/blue dial", and "ABS temp/red dial".
* *Max LED* - Chamber lighting is 30% brightness by default. While pressed, this button will temporary increase the brightness to 100%.
* *Microstep up* - Increases nozzle-to-bed distance by .01mm.
* *Microstep down* - Decreases nozzle-to-bed distance by .01mm.

![Voron Trident Skirt Buttons](../../../../assets/images/voron-trident-skirt-buttons-2.jpg)
*Skirt buttons*
{: .fs-2 .text-grey-dk-000 }

The construction of a button consists of four parts; (1) cover, (2) mechanical switch, (3) housing, and (4) lock ring.

![Exploded view of Meteyou's GCode Button](../../../../assets/images/gcode-button-exploded.png)
*Exploded view of Meteyou's GCode Button*
{: .fs-2 .text-grey-dk-000 }

The mechanical switch is held in the housing, which is inserted through the front of a skirt hex opening, and secured in place from behind with a lock ring. I kept the wiring as simple as possible. One con is that, because the LEDs are installed in the switch housing, they are south facing and the lighting is uneven.

* LEDs - Each mechanical switch has an embedded 2x3x4 LED, with the leads poking out the bottom. The positive leads and negative leads are wired inline, and terminate in a MicroFit connector. Since I just want the LEDs on when the printer is powered, any 5V source and ground pin will work and there is no logic/data pins/extra hardware to worry about.

![Skirt Button LED Wiring](../../../../assets/images/skirt-buttons-wiring-leds.jpg)
*Skirt Button LED Wiring*
{: .fs-2 .text-grey-dk-000 }

* Mechanical Switches - Each mechanical switch has two pins; ground and signal. The ground pins don't play a role in the functionality, so all the ground pins can be wired together. The signal pins will each have their own wire so that when pressed, the short can be detected. The 5 wires are then combined in a 5-pin MicroFit. On the other end of each signal wire, they connect to available GPIO ports. I was not able to get this working with the Raspberry Pi's GPIO pins though, and ended up using pins on my Fysetc Spider v1.1.

![Skirt Button Switch Wiring](../../../../assets/images/skirt-buttons-wiring-diagram.png)
*Skirt Button Switch Wiring*
{: .fs-2 .text-grey-dk-000 }

![Skirt Button Wiring Complete](../../../../assets/images/skirt-buttons-wiring-complete.jpg)
*Skirt Button Wiring Complete*
{: .fs-2 .text-grey-dk-000 }

The button macros are also easy to set up. Here's an example for my "microstep up" button:

```
[gcode_button BUTTON_MICROSTEP_UP]
pin: ^!PC2
press_gcode:
    SET_GCODE_OFFSET Z_ADJUST=0.01
release_gcode:
```

And for my "Max LED" button to see how to handle on-press events:

```
[gcode_button BUTTON_CASELIGHT]
pin: ^!PB13
press_gcode:
    SET_PIN PIN=caselight VALUE=1
release_gcode:
    SET_PIN PIN=caselight VALUE=0.3
```

And, lastly, I created some custom buttons:

![Custom Buttons](../../../../assets/images/skirt-buttons-custom-buttons.png)
*Custom Buttons*
{: .fs-2 .text-grey-dk-000 }

To get the LEDs to shine through, I did a filament swap between layers 4 and 5. This results in the fronts of the buttons using my secondary color, KVP Graphite ABS, and the rest of the buttons (including the icon's fill) using MH Build Series White ABS. Even though I used an opaque plastic rather than a transparent plastic, I find the glow to be acceptable.

[Download the STL files for my custom buttons](../../../../assets/files/button-covers.zip){: .btn .btn-purple}

### Killw2k's LCD Display Tweak - Remaining Time

I found [Killw2k's LCD Display Tweak - Remaining Time](https://www.reddit.com/r/VORONDesign/comments/rv9oxn/lcd_status_screen_tweak/) mod on reddit. All it does is move the progress bar to the bottom row to make room for displaying remaining time and total time, neither of which are shown by default.

### Future Mods to Consider
* GitHub - [Yeri's Magnetic Panels](https://github.com/Yeriwyn/VoronUsers/tree/V1-and-V2-panels/printer_mods/yeri/V1_V2_Trident_Magnetic_Panels) - His .f3d file is parametric, which is handy because I only have 1mm foam tape on the side panels. These panel clips are not compatible with 'Stury Handles'. [Alternative handle from 2.2](https://github.com/VoronDesign/Voron-2/blob/Voron2.2/STLs/VORON2.2/Panel_Mounting/Handles_Panel_Rests_Misc/handle_3mm_x2_Rev1.stl).
* GitHub - [Slidr666's OV5648 Camera Mount](https://github.com/Slidr666/VoronUsers/tree/master/printer_mods/Slidr/PanzerObserver2.4) - Originally seen on [SteveBuild's 2.4r2 update stream](https://www.youtube.com/watch?v=J2RGA8Az7eY).

## iv. Slicer Stuff
* GitHub - [AndrewEllis93's PIF Profile](https://github.com/AndrewEllis93/Ellis-PIF-Profile)
* [SuperSlicer Bed Model](https://github.com/hartk1213/MISC/tree/main/Voron%20Mods/SuperSlicer)
* [My Bed Texture](../../../../assets/images/superslicer-bed-plain.png)
