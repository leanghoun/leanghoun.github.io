---
layout: default
title: Mods & Tweaks
parent: Voron Trident
permalink: /docs/collections/voron-trident/mods-tweaks
nav_order: 3
---

# Mods & Tweaks

#### Quick Links
* [Meteyou's GCode Buttons](#meteyous-gcode-buttons)
* [Funny Pack](#funny-pack)
* [Panel Lockers](#panel-lockers)
* [Sturdy Handles](#sturdy-handles)
* [6-pin MicroFit Skirt Insert + Lock](#6-pin-microfit-skirt-insert)
* [StealthBurner Beta](#stealthburner-beta)
* [Eddie's LED Bar Clip](#eddies-led-bar-clip)
* [Killw2k's LCD Display Tweak - Remaining Time](#killw2ks-lcd-display-tweak---remaining-time)
* [Future Mods to Consider](#future-mods-to-consider)

## Meteyou's GCode Buttons

I like [Meteyou's GCode Buttons](https://github.com/VoronDesign/VoronUsers/tree/master/legacy_printers/printer_mods/meteyou/gcode_buttons) because they use mechanical keyboard switches for satisfying tactility and are simple to light up with embedded 2x3x4 LEDs.

Preheat
: Cycles between "cooldown/white dial", "PLA temp/blue dial", and "ABS temp/red dial".

Max LED
: Chamber lighting is 30% brightness by default. While pressed, this button will temporary increase the brightness to 100%.

Microstep up
: Increases nozzle-to-bed distance +0.01mm.

Microstep down
: Decreases nozzle-to-bed distance −0.01mm.

![Voron Trident Skirt Buttons](../../../../assets/images/voron-trident-skirt-buttons-2.jpg)
*Skirt buttons*
{: .fs-2 .text-grey-dk-000 }

The construction of a button consists of four parts; (1) button, (2) mechanical switch, (3) housing, and (4) lock ring. The mechanical switch is held in the housing, which is inserted through the front of a skirt hex opening, and secured in place from behind with a lock ring.

![Exploded view of Meteyou's GCode Button](../../../../assets/images/gcode-button-exploded.png)
*Exploded view of Meteyou's GCode Button*
{: .fs-2 .text-grey-dk-000 }

I kept the wiring as simple as possible. One con is that, because the LEDs are installed in the switch housing, they are south facing and the lighting is uneven.

**LEDs** - Each mechanical switch has an embedded 3V 2x3x4 LED, with the leads poking out the bottom. The positive leads and negative leads are wired inline, and terminate in a MicroFit connector. Since I just want the LEDs on when the printer is powered, I used the Raspberry Pi's 3V3 power pin and ground pin.

![Skirt Button LED Wiring](../../../../assets/images/skirt-buttons-wiring-leds.jpg)
*Skirt Button LED Wiring*
{: .fs-2 .text-grey-dk-000 }

**Mechanical Switches** - Each mechanical switch has two pins; ground and signal. The ground pins don't play a role in the functionality, so all the ground pins can be wired together. The signal pins will each have their own wire so that when pressed, the short can be detected. The 5 wires are then combined in a 5-pin MicroFit. On the other end of each signal wire, they connect to available GPIO ports. I was not able to get this working with the Raspberry Pi's GPIO pins though, and ended up using pins on my Fysetc Spider v1.1.

![Skirt Button Switch Wiring](../../../../assets/images/skirt-buttons-wiring-diagram.png)
*Skirt Button Switch Wiring*
{: .fs-2 .text-grey-dk-000 }

![Skirt Button Wiring Complete](../../../../assets/images/skirt-buttons-wiring-complete.jpg)
*Skirt Button Wiring Complete*
{: .fs-2 .text-grey-dk-000 }

The button macros are also easy to set up. You need a pin assignment, "on press" actions, and "on release" actions. Here's an example for my "microstep up" button:

```yaml
[gcode_button BUTTON_MICROSTEP_UP]
pin: ^!PC2
press_gcode:
    SET_GCODE_OFFSET Z_ADJUST=0.01
release_gcode:
```

And for my "max LED" button to see how to handle a button "while pressed":

```yaml
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

## Funny Pack

The [Funny Pack](https://github.com/thiagolocatelli/Voron/tree/master/Mods/funny_pack) is based on the [Fanny Pack](https://github.com/oab1/VoronMods/tree/main/v2.2%20Recirculating%20Filter) which is in turn based on the [Nevermore](https://github.com/nevermore3d), this exhaust filter uses dual 5015 fans to circulate air through [activated carbon pellets](https://envirosupply.net/products/4mm-pellet-virgin-coal-activated-carbon-charcoal-for-vapor-filtration-1-lb-bag) ([alternative source](https://www.amazon.com/EnviroSupply-Premium-Bituminous-Activated-Charcoal/dp/B00XNXC70W)). I ended up needing to print mesh inserts to prevent pellets from falling out of the basket.

## Titanium Backers

The aluminum frame undergoes some amount of [thermal expansion](https://github.com/tanaes/whopping_Voron_mods/tree/main/extrusion_backers) as the chamber heats up. One way to counteract this is to brace the key extrusions with a secondary type of metal. Stainless steel backers are cheaper, but heavier. I sourced titanium backers from [3DMakerParts](https://3dmakerparts.com/products/titanium-extrusion-backers-v2-4-trident?variant=40926558093519) and the add-ons for M3x6 screws, M3x8 screws, and M3 t-nuts.

![Titanium Backers from 3DMakerParts](../../../../assets/images/voron-trident-ti-backers-finish-1.jpg)
*Titanium Backers from 3DMakerParts - Logo*
{: .fs-2 .text-grey-dk-000 }

![Titanium Backers from 3DMakerParts](../../../../assets/images/voron-trident-ti-backers-finish-2.jpg)
*Titanium Backers from 3DMakerParts - Chain Mounts*
{: .fs-2 .text-grey-dk-000 }

![Titanium Backers from 3DMakerParts](../../../../assets/images/voron-trident-ti-backers-finish-3.jpg)
*Titanium Backers from 3DMakerParts*
{: .fs-2 .text-grey-dk-000 }

## Panel Lockers

These [Panel Lockers](https://github.com/v6cl/My-Voron2.4-Customs/tree/main/Panel_Locker) are print-in-place, work with 1mm-foam-lined side panels, and have good clamping force. Has two drawbacks; (1) one face of the model prints at an angle and catches light badly, and (2) you can't put two lockers on adjacent panels in the same location. Considering replacing them with [this design](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/richardjm/snap-latch-2020), that uses filament as a hinge, or [Yeri's Magnetic Clips](https://github.com/Yeriwyn/VoronUsers/tree/V1-and-V2-panels/printer_mods/yeri/V1_V2_Trident_Magnetic_Panels/STL/Trident/300).

## Sturdy Handles

[Sturdy Handles](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/jeoje/Sturdy_Handles) mount well and do not interfere with panel removal, but the extrusions have a tendency to rotate. Need to remember to periodically retighten the frame.

## 6-pin MicroFit Skirt Insert

Two sources for this modd; [6-pin MicroFit Skirt Insert](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/StvPtrsn/Parts_Jigs_and_Mods/Parts) and the [Lock](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Jon/adxl345_skirt_keystone/STL). Provides an interface for the ADXL345 cable to make Input Shaper calibration easier.

## StealthBurner Beta

Using [StealthBurner Beta](https://github.com/VoronDesign/Voron-Afterburner/tree/sb-beta/STLs/Stealthburner) on top of the new ClockWork1 printed front. And using Hartk's PCB cover to contain the wiring though I do not have a toolhead PCB.

## Eddie's LED Bar Clip

Everyone likes [Eddie's LED Bar Clip](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/eddie/LED_Bar_Clip). Easy to print, clips directly to 2020 extrusions, and have baffles to shield light from eyes. I did not extend the LED mounts fully from front to back, and chose to leave some room. Just in case I need space to mount a camera in the future. Check out [Steve Build's stream](https://www.youtube.com/watch?v=qTTLXU41Q0o&t=5188s) to see how to wire them together into one 4-pin dupont connector.

## Killw2k's LCD Display Tweak - Remaining Time

I found [Killw2k's LCD Display Tweak - Remaining Time](https://www.reddit.com/r/VORONDesign/comments/rv9oxn/lcd_status_screen_tweak/) mod on reddit. All it does is move the progress bar to the bottom row to make room for displaying remaining time and total time, neither of which are shown by default.

## Future Mods to Consider

* GitHub - [Yeri's Magnetic Panels](https://github.com/Yeriwyn/VoronUsers/tree/V1-and-V2-panels/printer_mods/yeri/V1_V2_Trident_Magnetic_Panels) - His .f3d file is parametric, which is handy because I only have 1mm foam tape on the side panels. These panel clips are not compatible with 'Sturdy Handles'. [Alternative handle from 2.2](https://github.com/VoronDesign/Voron-2/blob/Voron2.2/STLs/VORON2.2/Panel_Mounting/Handles_Panel_Rests_Misc/handle_3mm_x2_Rev1.stl).
* GitHub - [Slidr666's OV5648 Camera Mount](https://github.com/Slidr666/VoronUsers/tree/master/printer_mods/Slidr/PanzerObserver2.4) - Originally seen on [SteveBuild's 2.4r2 update stream](https://www.youtube.com/watch?v=J2RGA8Az7eY).
* GitHub - [Frame Thermal Expansion Package](https://github.com/Deutherius/TECPac) - Both hardware and software.
* Better Filtration System, Discord@PF VT.520
  - [4" Inline Duct Fan](https://www.amazon.com/VIVOSUN-Australia-Charcoal-Pre-filter-Reversible/dp/B01DXYMBU6)
  - [HEPA filters](https://www.amazon.com/dp/B088Z7CLKC)
  - [4" Ducting](https://www.amazon.com/dp/B07WW7CY9F)
