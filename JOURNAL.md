---
title: "XT-1"
author: "redbigz"
description: "Modular CoreXY 3D Printer with a focus on repairability."
created_at: "2025-07-15"
---

**Total time:** 7 hours

# Table Of Contents (by Date)

- [2025-07-15](#2025-07-15---research)
- [2025-07-16](#2025-07-16---more-research--pcb-design))

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
