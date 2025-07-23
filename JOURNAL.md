---
title: "XT-1"
author: "redbigz"
description: "Modular CoreXY 3D Printer with a focus on repairability."
created_at: "2025-07-15"
---

**Total time:** 52 hours

# Checklist

## Pre-Design

- [x] Research
- [x] Part Picking

## Design

- [x] T-Plug
  - [x] Female Connector
  - [x] Male Connector
- [x] Toolhead _(note: excl. part cooling fans as they're modules)_
  - [x] Hotend
  - [x] Extruder
  - [x] Electronics
- [x] Gantry
- [ ] Bed
- [ ] Base
  - [ ] Base Extrusions
- [x] Modules
  - [x] 5015 Part Cooling Fan
- [ ] Motherboard
  - [x] Schematic
  - [ ] PCB

# Table Of Contents (by Date)

- [2025-07-15](#2025-07-15---research)
- [2025-07-16](#2025-07-16---more-research--pcb-design)
- [2025-07-17](#2025-07-17---starting-pcb-design)
- [2025-07-18](#2025-07-18---cad-designing-and-fixes)
- [2025-07-19](#2025-07-19---toolhead)
- [2025-07-20](#2025-07-20---more-toolhead)
- [2025-07-21](#2025-07-21---fan-ducts-was-pretty-unproductive)
- [2025-07-22](#2025-07-22---gantry)
- [2025-07-23](#2025-07-23---gantry--supplementary-motherboard)

# 2025-07-15 - Research

I've been researching today about 3D printer parts and brainstorming all the logistics behind this modular system.

**Estimated time:** 4 hours

## Designing Factors

- I want my printer to be easily user-repairable without any issues (taking inspiration from Framework devices)
- Single/two common screw heads used throughout the build (I'm thinking of Torx T10 or T5)
- _Attempting_ to do a heated bed
- Controlled via a socketed Pi CM3/CM4 (Klipper)
- SUPER EASY TO DISASSEMBLE!
- A triple module bay on the toolhead which can be hotswapped while the printer is on (for e.g. filament sensor, RGB, resonance tester, camera, laser cutter :3), using pogo pins and a dovetail system

## Part Ideas

### Base

- As suggested by Evan Le, I'm going with 2020 T-shape Aluminium Extrusions
- MGN12H or MGN9H rails
- CoreXY gantry

## Electronics Ideas

### Internals

- Socketed Pi CM3/CM4 on a custom daughterboard
- Socketed RP2040-based (custom?) motherboard
- TMC2209 Steppers
- Mean Well LRS-350-24 PSU

### Toolhead

- CR-Touch
- Lancer Melt Zone Long Hotend
- Nema 17 Steppers
- 3 Dovetail Bays for fans & expansions

# 2025-07-16 - More research & PCB design

**Estimated time:** 3 hours

## On Pi Compute Modules

For designing a motherboard with the Pi 4, I'll need to solder Hirose `DF40C-100DS-0.4v` connectors, which are SMD.

## Designing the PCB (and failing)

I got about this much done in terms of an Ethernet connection (MagJack) before calling quits. **I'm now deciding to run a regular Raspberry Pi 4 and use a stock motherboard such as the BTT SKR MINI.**

![epic fail](img/2025/07/16/skill_issue.png)
<br>
Figure 1 - _After hours of reading datasheets, all I could make was this._

# 2025-07-17 - Starting PCB design

**Estimated time:** 5 hours

## The Dovetail Plug system

(also known as the tail plug system 😬😬😬, i'll be shortening it to t-plug from here on out)

![image of the glorious t-plug schematic](img/2025/07/17/tplug-schem.png)
<br>
Here is the system for swappable toolhead attachments. I've decided on these main points:

- The CR-Touch will NOT use the attachment system as it requires multiple grounds and for the Z stepper to be on the same MCU (not happening)
- The 5V and 24V PWM inputs will be turned on as soon as both **CONT** pins are connected (in the event of a connection)
- One UART bus will be connected for the center module (the Pi Pico only has two UART buses and one needs to be used to connect to the Linux Pi)

I took the time to figure out KiCad and make the necessary symbols and footprints for the t-plug.

Here is the female PCB, using a JST-PH to communicate with the extruder board:
![t-plug female pcb](img/2025/07/17/pcb.png)
![t-plug female pcb but in 3d :3](img/2025/07/17/3d.png)
<br>
_look at my princess isnt she bootiful_

# 2025-07-18 - CAD Designing and fixes

**Estimated time:** 6 hours

## Plug Design

i've got the thing in OnShape now, and designed a dovetail system for keeping the pogo pins in place.

![t-plug in cad!](img/2025/07/18/tplug_cad.png)

## Base Design

![base number 0](img/2025/07/18/base_0.png)

## Fixes

### Shorting avoidance on the T-plug

![fixed t-plug schematic](img/2025/07/18/fixed_tplug.png)

I moved ground away from the powered pads to avoid pogo pins shorting due to proximity when sliding. I also changed the pad size of the female receptacle to avoid such proximity (as the pins are 0.9mm and the gap was 0.5mm):

![smaller pads!](img/2025/07/18/smaller_pads.png)

![tplug female pcb, fixed](img/2025/07/18/tp_fem_pcb_3d.png)

# 2025-07-19 - Toolhead

**Estimated time:** 8 hours

I'm pretty tired so I'll cut to the chase here. I made about 70% of the toolhead, and the only things left are the electronics and fans.

Using a [ProtoXtruder](https://github.com/nhchiu/3DPrinter-Designs/tree/main/ProtoXtruder_2.0) for the extruder, with a Nema 14 36mm Round Pancake motor (10T gear)

![toolhead](img/2025/07/19/printhead1.png)
![toolhead](img/2025/07/19/printhead2.png)

UPDATE: Fixed some heights to make it stronger:

![toolhead fixed](img/2025/07/19/printhead3.png)

# 2025-07-20 - More Toolhead

**Estimated time:** 7 hours

## Finished\* Toolhead

I've added:

- a 4010 fan (Noctua)
- a belt holder (which doubles as a CR-Touch mount)
- two t-plug bays (I know I said three but there isn't much of a use with three considering the CR-Touch isn't a module)

![the finished toolhead, apart from modules.](img/2025/07/20/th1.png)
![the back side of the toolhead](img/2025/07/20/th2.png)

Speaking of which, here is the male t-plug connector:

![male t-plug connector](img/2025/07/20/tpm1.png)
![back side of the male t-plug](img/2025/07/20/tpm2.png)
![pcb screenshot of the male t-plug](img/2025/07/20/tpm3.png)
![3d view of the male t-plug in kicad](img/2025/07/20/tpm4.png)

There's just enough clearance for the connection to the female bay (1.5mm) :3

# 2025-07-21 - Fan Ducts! (was pretty unproductive)

**Estimated time:** 5 hours

Today was pretty unproductive. I only managed to get two 5015 fan modules done. Due to the sliding mechanism, the fan module won't slide in unless the fans are screwed in after the frame is slid in.

You gotta admit it looks cool though:

![cool toolhead](img/2025/07/21/th1.png)

# 2025-07-22 - Gantry

**Estimated time:** 6 hours

I got a really productive session in CAD today. I've got the toolhead set up on a 360x360 gantry, along with the motor mounts and X axis idlers.

![the gantry!](img/2025/07/22/gantry1.png)

Here's the dual-idler design I came up with (took some inspiration from other CoreXY printers):

![an x-axis dual-idler mount](img/2025/07/22/idler1.png)

I'm basing my belt setup based on this image found in the [Anicept Vex CoreXY](https://highway.hackclub.com/guides/anicept-vex-corexy) guide in Highway:

![anicept corexy image](img/2025/07/22/anicept_corexy.png)

# 2025-07-23 - Gantry & (Supplementary) Motherboard

**Estimated time:** 8 hours

I'm pretty tired (again), so I'll just recount what I did.

I finished my gantry in its entirety:

![finished gantry](img/2025/07/23/gantry1.png)

I made custom mounts for all the idlers, and worked out a belt path that *barely* works. I'll tweak it while building the thing, since I'm starting to run out of time before Highway ends. I've worked out a gantry area of about 190x180 for the toolhead.

Also, I've started work on a supplementary motherboard (yep, this lil guy has two moms!). It holds three limited ports for the t-plug system (lacking CONT due to a gpio shortage), with one having access to the secondary UART bus. Here's the finished schematic:

![motherboard schematic](img/2025/07/23/mobo1.png)