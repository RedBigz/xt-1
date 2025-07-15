---
title: "XT-1"
author: "redbigz"
description: "Modular CoreXY 3D Printer with a focus on repairability."
created_at: "2025-07-15"
---

# Table Of Contents (by Date)
- 2025-07-15
    - [Research](#2025-07-15---research)

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
