---
layout: default
title: Gryphon & Gryphle0n
parent: Blasters
grand_parent: Collections
permalink: /docs/blasters/gryphon/
nav_order: 2
---

# Gryphon & Gryphle0n
{: .no_toc }

#### Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## Introduction

The Gryphon is an open-source flywheel blaster designed by Flygonial and available on [Github](https://github.com/Flygonial/The-Gryphon-Foam-Dart-Blaster). Most up to date CAD files can be found [here](https://a360.co/2N3szi3).

### Features

*(Pulled from the Github page)*

- Uses 130 to 180 sized 20.4mm , brushed DC motors.
- Semi-auto by rack and pinion with 1:3 gear multiplication. The trigger pull is fairly short at 12mm.
- Accepts 33 to 38mm OD flywheels (all 2mm shaft fit, superstock upgrade flywheels).
- Utilizes a horizontal flywheel cage that bolts directly onto the magwell. This is a mounting pattern less prone to misalignment than a Stryfe's mounting bosses or similar.
- Accepts Worker Talon mags, Katana-geometry mags with a lower release cut-out, and almost all full-length magazines.
- Battery is located in the stock or a side battery tray.
- Full-length feed guide integrated in magwell for maximum feeding reliability.
- Bore-axis is almost as close as possible to top rail of blaster, which is theoretically more intuitive to aim with.
- Will fit on build volume as small as 120 mm3.

In my opinion, the Gryphon platform is solid, easy to print, relatively easy to assemble, and offers a lot of modding and upgrade potential. The Gryphle0n is my slightly modified version where superfluous decorations have been removed, some parts tweaked for better printability, and utilizes heatset inserts anywhere screws go directly into plastic.

![Gryphle0n & Gryphon](../../../../assets/images/gryphle0n-00-both.jpg)
*Gryphle0n & Gryphon*
{: .fs-2 .text-grey-dk-000 }
{: .no_toc }

![Gryphle0n Front](../../../../assets/images/gryphle0n-00-front.jpg)
*Gryphle0n Front*
{: .fs-2 .text-grey-dk-000 }

![Gryphle0n Grip](../../../../assets/images/gryphle0n-00-grip.jpg)
*Gryphle0n Grip*
{: .fs-2 .text-grey-dk-000 }

![Gryphle0n Middle](../../../../assets/images/gryphle0n-00-middle.jpg)
*Gryphle0n Middle*
{: .fs-2 .text-grey-dk-000 }

![Gryphle0n Top](../../../../assets/images/gryphle0n-00-top.jpg)
*Gryphle0n Top*
{: .fs-2 .text-grey-dk-000 }

## Build Guide

### BOM

- [ ] 2 x 130/180 motors
- [ ] 33-38mm, 2mm shaft-fit flywheels
- [ ] 16-18AWG multi-strand hobby wire
- [ ] XT60/XT30 connectors (2 female, 1 male)
- [ ] Heatshrink
- [ ] 21A full-size microswitch
- [ ] 2 x 20mm steel pins
- [ ] 0.5mm coil thickness, 5mm diameter, 15mm compression spring
- [ ] 0.5mm coil thickness, 5mm diameter, 50mm compression spring
- [ ] 4 x M2x4 FHCS
- [ ] 8 x M3x6 SHCS
- [ ] 22 x M3x8 SHCS
- [ ] 2 x M3x10 SHCS
- [ ] 4 x M3x12 SHCS
- [ ] 1 x M3x16 SHCS
- [ ] 2 x M3x20 SHCS
- [ ] 4 x M3x25 SHCS
- [ ] 4 x M3 nuts (Gryphon) or 34 x M3 heatset inserts (Gryphle0n)
{: .fs-2 }

### Cage

![Mount Motors](../../../../assets/images/gryphle0n-01-motors.jpg)
*Mount Motors*
{: .fs-2 .text-grey-dk-000 }

Double check the motors' polarities, make sure the motors are fully seated, and that the shafts appear parallel to each other and perpendicular to the mounting.

- [ ] 4 x M2x4 FHCS
{: .fs-2 }

![Mount Flywheels](../../../../assets/images/gryphle0n-03-flywheels.jpg)
*Mount Flywheels*
{: .fs-2 .text-grey-dk-000 }

![Check Flywheels' Alignment](../../../../assets/images/gryphle0n-02-flywheels.jpg)
*Check Flywheels' Alignment*
{: .fs-2 .text-grey-dk-000 }

When press-fitting the flywheels, get them as even as possible with the flywheels' middles centered to the dart hole. Additionally, check to make sure they aren't binding and don't rub against any plastic as they turn.

![Install Flywheels' Cover](../../../../assets/images/gryphle0n-04-flywheels-covered.jpg)
*Install Flywheel Cover*
{: .fs-2 .text-grey-dk-000 }

- [ ] 2 x M3x8 SHCS
{: .fs-2 }

![Out of Darts' Motor Spanning Board](../../../../assets/images/gryphle0n-05-motor-pcb.jpg)
*Out of Darts' Motor Spanning Board*
{: .fs-2 .text-grey-dk-000 }

[Out of Darts' Motor Spanning Board](https://outofdarts.com/collections/electronics/products/flywheel-motor-spanning-board-super-easy-flywheel-soldering) makes wiring up the motors a bit easier. The PCB handles the inter-motor connections and you only have to deal with a pair of wires leading to the first XT60 female connector.

![Place Motor Spacers](../../../../assets/images/gryphle0n-06-motor-spacers.jpg)
*Place Motor Spacers*
{: .fs-2 .text-grey-dk-000 }

The motor spanning board comes with some printed spacers to give some clearance and prevent shorts. Place them like so.

![Spanning Board Soldered](../../../../assets/images/gryphle0n-07-motor-pcb-soldered.jpg)
*Spanning Board Soldered*
{: .fs-2 .text-grey-dk-000 }

![Solder Wires for XT60 Connector](../../../../assets/images/gryphle0n-08-motors-wired.jpg)
*Solder Wires for XT60 Connector*
{: .fs-2 .text-grey-dk-000 }

![Install Motors' Cover](../../../../assets/images/gryphle0n-09-motors-covered.jpg)
*Install Motors' Cover*
{: .fs-2 .text-grey-dk-000 }

- [ ] 2 x M3x8 SHCS
- [ ] 1 x M3x20 SHCS
{: .fs-2 }

![Check Wires Against Magwell for Length](../../../../assets/images/gryphle0n-10-motor-connector-length.jpg)
*Check Wires Against Magwell for Length*
{: .fs-2 .text-grey-dk-000 }

Feed the wires through the magwell to get a feel for the length required. The XT60 connector here will sit underneath a wire cover.

![Solder and Heatshrink the XT60 Female Connector](../../../../assets/images/gryphle0n-11-motor-XT60.jpg)
*Solder and Heatshrink the XT60 Female Connector*
{: .fs-2 .text-grey-dk-000 }

Don't forget to place the heatsinks on the wires before soldering to the XT60 female connector. In this particularly case, the motors were oriented per the PCB's markings, but still ended spinning the wrong way, so I inverted the XT60 to correct it.

### Magwell

![Attaching Magwell](../../../../assets/images/gryphle0n-12-attaching-magwell.jpg)
*Attaching Magwell*
{: .fs-2 .text-grey-dk-000 }

- [ ] 4 x M3x8 SHCS
{: .fs-2 }

![Magwell attached](../../../../assets/images/gryphle0n-13-magwell-attached.jpg)
*Magwell attached*
{: .fs-2 .text-grey-dk-000 }

### Grip

![Grip](../../../../assets/images/gryphle0n-14-grip.jpg)
*Grip*
{: .fs-2 .text-grey-dk-000 }

![Grip with Switch Posts](../../../../assets/images/gryphle0n-15-switch-standoffs.jpg)
*Grip with Switch Posts*
{: .fs-2 .text-grey-dk-000 }

Install the two screws that form the switch seating posts.

- [ ] 2 x M3x10 SHCS
{: .fs-2 }

![Switch Placement](../../../../assets/images/gryphle0n-16-switch-placement.jpg)
*Switch Placement*
{: .fs-2 .text-grey-dk-000 }

The 21A switch sits like so.

![Required Wires](../../../../assets/images/gryphle0n-17-switch-wire-lengths.jpg)
*Required Wires*
{: .fs-2 .text-grey-dk-000 }

Positive wire (blue) has two runs; one from the motors to the switch, and one from the switch to the battery. We'll be using NO and COM terminals to power the motors only when the trigger is pressed. Negative wire (white) goes directly from the motors to the battery.

![Finish the Motors' XT60 Connector](../../../../assets/images/gryphle0n-18-magwell-XT60.jpg)
*Finish the Motors' XT60 Connector*
{: .fs-2 .text-grey-dk-000 }

Solder the wires to the XT60 male connector, connect it to the motors, then feed the wires through the top cover.

![Solder the 21A Switch](../../../../assets/images/gryphle0n-19-switch-positive-wire.jpg)
*Solder the 21A Switch*
{: .fs-2 .text-grey-dk-000 }

Solder the other end of the motors-to-switch positive wire and one end of the switch-to-battery wire to the NO and COM terminals of the switch. It does not matter which wire goes to NO and COM.

![Install Switch Trigger and Tuck Wires](../../../../assets/images/gryphle0n-20-switch-trigger.jpg)
*Install Switch Trigger and Tuck Wires*
{: .fs-2 .text-grey-dk-000 }

Assemble and install the switch trigger. Apply a bit of silicone grease to smoothen the action. Wires will tuck like so.

- [ ] 1 x M3x6 SHCS
{: .fs-2 }

![Install the Pusher](../../../../assets/images/gryphle0n-21-pusher.jpg)
*Install the Pusher*
{: .fs-2 .text-grey-dk-000 }

Install the pusher with the teeth on the far side and closer to the rear of the grip. Apply a bit of silicone to the sides of the pusher to smoothen the action.

![Install the Trigger](../../../../assets/images/gryphle0n-22-trigger.jpg)
*Install the Trigger*
{: .fs-2 .text-grey-dk-000 }

Install the trigger with the spring. Depending on print quality and spring strength, you may need a second spring to ensure that the trigger and pusher returns to the original positions. Apply a bit of silicone grease to area around the post and spring to smoothen the action.

![Install the Toothed Gear](../../../../assets/images/gryphle0n-23-gear.jpg)
*Install the Toothed Gear*
{: .fs-2 .text-grey-dk-000 }

Install the toothed gear and line up the center hole with the receiving hole in the grip. Apply a bit of silicone grease to the faces of the gear to smoothen the action.

![Install Grip Cover and Toothed Gear Shaft](../../../../assets/images/gryphle0n-24-grip-cover.jpg)
*Install Grip Cover and Toothed Gear Shaft*
{: .fs-2 .text-grey-dk-000 }

Secure the grip cover with an M3 screw, and insert the 2mm shaft through the cover, toothed gear, and grip frame.

- [ ] 1 x M3x6 SHCS
{: .fs-2 }

![Close Top Cover](../../../../assets/images/gryphle0n-25-grip-to-magwell.jpg)
*Close Top Cover*
{: .fs-2 .text-grey-dk-000 }

Close up the top cover. This part is fiddly. Wires should stay tucked *behind* the toothed gear and not impede the gear rotation. There's a notch in the cover to accommodate the shaft.

![Secure Mag Release](../../../../assets/images/gryphle0n-26-mag-release-spring.jpg)
*Secure Mag Release*
{: .fs-2 .text-grey-dk-000 }

Secure the mag release switch with an M3 screw.

- [ ] 1 x M3x16 SHCS
{: .fs-2 }

![Install Spring and Connect Magwell with Grip](../../../../assets/images/gryphle0n-27-grip-installed.jpg)
*Install Spring and Connect Magwell with Grip*
{: .fs-2 .text-grey-dk-000 }

Place the mag release spring between the magrelease switch and grip frame, and insert the grip into the magwell. This is a good opportunity to test the trigger action. The trigger and pusher should extend and return with no sticking. Watching the action from the bottom of the magwell, you should see the pusher extend forward and retract all the way. If the pusher does not retract fully, it will prevent darts from feeding properly.

![Install Magwell Wire Cover](../../../../assets/images/gryphle0n-28-magwell-wire-cover.jpg)
*Install Magwell Wire Cover*
{: .fs-2 .text-grey-dk-000 }

Install the wire cover over the XT60 connector.

- [ ] 2 x M3x6 SHCS
{: .fs-2 }

![Install Right Scale](../../../../assets/images/gryphle0n-29-right-scale.jpg)
*Install Right Scale*
{: .fs-2 .text-grey-dk-000 }

Install the right scale.

- [ ] 2 x M3x6 SHCS
{: .fs-2 }

![Install Left Scale](../../../../assets/images/gryphle0n-30-left-scale.jpg)
*Install Left Scale*
{: .fs-2 .text-grey-dk-000 }

Install the left scale.

- [ ] 2 x M3x6 SHCS
{: .fs-2 }

![Install Remaining Screws](../../../../assets/images/gryphle0n-31-fastened.jpg)
*Install Remaining Screws*
{: .fs-2 .text-grey-dk-000 }

Secure the magwell, grip, and top cover with through screws.

- [ ] 4 x M3x25 SHCS
{: .fs-2 }

### Stock

![Check Wire Length](../../../../assets/images/gryphle0n-32-stock-wire-lengths.jpg)
*Check Wire Length*
{: .fs-2 .text-grey-dk-000 }

The wires need to feed through the buffer tube with a extra few inches to make it easy to handle the battery.

![Finish XT60 Connector](../../../../assets/images/gryphle0n-33-stock-XT60.jpg)
*Finish XT60 Connector*
{: .fs-2 .text-grey-dk-000 }

Add heatshrink and solder the wires to an XT60 female connector.

![Stock Parts](../../../../assets/images/gryphle0n-34-stock.jpg)
*Stock Parts*
{: .fs-2 .text-grey-dk-000 }

![Sling Mount and Buttplate Hook](../../../../assets/images/gryphle0n-35-buttplate-hook.jpg)
*Sling Mount and Buttplate Hook*
{: .fs-2 .text-grey-dk-000 }

Attach the sling mount to the top of the buffer tube (my printed part has no sling mount), and install the buttplate hook.

- [ ] 2 x M3x12 SHCS
- [ ] 1 x M3x8 SHCS
{: .fs-2 }

![Insert Locking Pin](../../../../assets/images/gryphle0n-36-stock-locking-pin.jpg)
*Insert Locking Pin*
{: .fs-2 .text-grey-dk-000 }

Insert the locking pin into the stock.

![Secure Lock Release](../../../../assets/images/gryphle0n-37-lock-release.jpg)
*Secure Lock Release*
{: .fs-2 .text-grey-dk-000 }

Install the lock release.

- [ ] 1 x M3x20 SHCS
{: .fs-2 }

![Add Spring](../../../../assets/images/gryphle0n-38-stock-spring.jpg)
*Add Spring*
{: .fs-2 .text-grey-dk-000 }

Add the spring. This spring needs to be strong enough to keep tension on the locking pin and prevent the stock from collapsing during use.

![Insert Buffer Tube](../../../../assets/images/gryphle0n-39-buffer-tube.jpg)
*Insert Buffer Tube*
{: .fs-2 .text-grey-dk-000 }

Insert the buffer tube.

![Feed XT60 Connector](../../../../assets/images/gryphle0n-40-stock-XT60.jpg)
*Feed XT60 Connector*
{: .fs-2 .text-grey-dk-000 }

Feed the XT60 connector through the buffer tube. It should stick out just a bit.

![Attach Stock to Grip](../../../../assets/images/gryphle0n-41-stock-attached.jpg)
*Attach Stock to Grip*
{: .fs-2 .text-grey-dk-000 }

Attach the stock to the grip. There's a screw on each side and two on the rear.

- [ ] 2 x M3x8 SHCS
- [ ] 2 x M3x12 SHCS
{: .fs-2 }

![Flash Hider and Picatinny Rails](../../../../assets/images/gryphle0n-42-flash-hider-picatinny.jpg)
*Flash Hider and Picatinny Rails*
{: .fs-2 .text-grey-dk-000 }

Attach the flash hider and picatinny rails.

- [ ] 9 x M3x8 SHCS
{: .fs-2 }

![Flash Hider and Picatinny Rails](../../../../assets/images/gryphle0n-43-flash-hider-picatinny-installed.jpg)
*Flash Hider and Picatinny Rails*
{: .fs-2 .text-grey-dk-000 }

Should look like this.

![Check Picatinny Spacing](../../../../assets/images/gryphle0n-44-flash-hider-picatinny-top.jpg)
*Check Picatinny Spacing*
{: .fs-2 .text-grey-dk-000 }

Double check the picatinny pattern spacing.

![Install Front Grip](../../../../assets/images/gryphle0n-45-front-grip.jpg)
*Install Front Grip*
{: .fs-2 .text-grey-dk-000 }

Install your front grip of choice.

- [ ] 2 x M3x8 SHCS
{: .fs-2 }

![Complete](../../../../assets/images/gryphle0n-46-complete.jpg)
*Complete*
{: .fs-2 .text-grey-dk-000 }

Your Gryphon/Gryphle0n is complete!