[![Support trans rights in Australia here](https://pride-badges.pony.workers.dev/static/v1?label=support+aussie+trans+rights+:3&labelColor=%23555&stripeWidth=8&stripeColors=5BCEFA%2CF5A9B8%2CFFFFFF%2CF5A9B8%2C5BCEFA)](https://auspath.org.au/project-491/)

## IMPORTANT

- The JST PH connectors from the t-plugs to the supp. board need to have reverse connectors!

# XT-1

![Stage: Approved](https://img.shields.io/badge/Stage-Approved!_(Let's_fucking_gooooooooo)-green?style=for-the-badge)
![GitHub commit activity](https://img.shields.io/github/commit-activity/w/RedBigz/xt-1?style=for-the-badge&logo=github)
[![Hack Club](https://img.shields.io/badge/Hack_Club-%23EC3750?style=for-the-badge&logo=hackclub&logoColor=white)](https://highway.hackclub.com)

A modular CoreXY 3D Printer with a focus on repairability.

| [READ THE JOURNAL](./JOURNAL.md) | [READ CAD CREDITS](CAD_CREDITS.md) |
| -------------------------------- | ---------------------------------- |

| ![A render of an XT-1 with a Benchy atop its bed](img/render/0001.png) | ![Gantry of an XT-1](img/render/0002.png)                  |
| ---------------------------------------------------------------------- | ---------------------------------------------------------- |
| ![Close-up of the toolhead/bed of the XT-1](img/render/0003.png)       | ![Close-up of the bottom of the XT-1](img/render/0004.png) |

## Who I am and why I made this

Hi, I'm May, a 15-year-old programmer and hardware enthusiast from Australia. I have spent the past few weeks developing a custom 3D printer based on the CoreXY motion system that allows for custom component bays to be inserted on the toolhead. I made this dovetail plug (t-plug) system to mimic the concept of [Framework](https://frame.work)'s laptop expansion bays. I believe expansion bays largely simplify repairs performed by consumers and allows for greater self-expression through custom designs that can be attached to the toolhead.

## What is this?

The XT-1 is a custom CoreXY 3D printer with two custom t-plug (as defined above) bays to transmit UART and 5V & 24V PWM signals for things such as:

- Accelerometers (not ADXL as they're SPI)
- Laser Diodes
- Fans

Here are some basic statistics for the printer:

- 2 t-plug bays
- 2WD CoreXY System
- 180x180x160 build volume
- ~360x360x420 external dimensions

# Gallery

## CAD Model

![Top-Left-Front view of the XT-1](img/cad/TLF.png)
![Top-Right-Back view of the XT-1](img/cad/TRB.png)

## Supplementary Board

![Pcbnew view of the Supplementary Board of the XT-1](img/pcb/supp.png)

## T-Plug

![Pcbnew view of the XT-1 male t-plug](img/pcb/male.png)
![Pcbnew view of the XT-1 female t-plug](img/pcb/female.png)

# Building

## CAD Models

To export parts, open the model in OnShape [here](https://cad.onshape.com/documents/9bd0c3164ed27c6437ee23ee/w/6070e846ece5dc4f933b41e5/e/3b4b9a8834f82e5e0afe2787) (I would suggest plugging in your computer before downloading, the models are hundreds of megs and just rendering them has crashed my desktop RX 7800XT over 10 times when rendering the full assembly)

To find the _assembly_ in .STEP format, check the `asm` folder in this repo.

## Wiring Diagram

![An electronic wiring diagram of the XT-1](img/wiring.png)

## Quick BOM

**Quick Note:** This BOM is made largely for Hack Club's [Highway grant program](https://highway.hackclub.com) and prices reference the sale price I am able to purchase each product at (as @ 29/07/2025) in AUD (with a AUD -> USD exchange rate of $0.66 per A$1).

| Manufacturer           | Item                                                                    | Size                | Qty | Units | Unit Cost (AUD) | Cost (AUD) | Cost (USD) | Link                                                              |
| ---------------------- | ----------------------------------------------------------------------- | ------------------- | --- | ----- | --------------- | ---------- | ---------- | ----------------------------------------------------------------- |
| BIGTREETECH            | BTT SKR Mini E3 V3                                                      | -                   | 1   | each  | 52.51           | 52.51      | 34.66      | https://www.aliexpress.com/item/1005003519869375.html             |
| JINGLIN                | 5/lot 4-lead NEMA 17                                                    | -                   | 1   | lot   | 69.39           | 69.39      | 45.80      | https://www.aliexpress.com/item/1005008510880419.html             |
|                        | 2/lot 5015 Turbo Fan                                                    | -                   | 1   | lot   | 4.90            | 4.90       | 3.23       | https://www.aliexpress.com/item/32970914615.html                  |
| JINGLIN                | 2/lot 4020 Fan                                                          | -                   | 1   | lot   | 5.09            | 5.09       | 3.36       | https://www.aliexpress.com/item/32972111881.html                  |
| Ancufy                 | NEMA 14 + 1M cable                                                      | -                   | 1   | each  | 14.89           | 14.89      | 9.83       | https://www.aliexpress.com/item/1005006423228157.html             |
| HighQ                  | 2/lot 2020 V-Slot Extrusions                                            | 280mm               | 2   | lot   | 14.79           | 29.58      | 19.52      | https://www.aliexpress.com/item/1005007310271857.html             |
|                        |                                                                         | 320mm               | 2   | lot   | 15.89           | 31.78      | 20.97      |                                                                   |
|                        |                                                                         | 360mm               | 2   | lot   | 16.69           | 33.38      | 22.03      |                                                                   |
| Magic Dragon           | 2020 V-Slot Extrusions                                                  | 300mm               | 1   | each  | 8.47            | 8.47       | 5.59       | https://www.aliexpress.com/item/1005004679698586.html             |
|                        | MGN12 Linear Rail                                                       | 300mm               | 1   | each  | 20.39           | 20.39      | 13.46      | https://www.aliexpress.com/item/1005003696820721.html             |
| CHY CNC                | 2/lot 8mm Linear Shaft (M4x8mm)                                         | 200mm               | 2   | lot   | 16.29           | 32.58      | 21.50      | https://www.aliexpress.com/item/1005008854590053.html             |
| SNWNYN                 | 2x MGN12H rails, 4x MGN Blocks                                          | 200mm               | 1   | lot   | 34.59           | 34.59      | 22.83      | https://www.aliexpress.com/item/1005005966099152.html             |
| 3D ManufacturinG       | T8 Lead Screw + Nut                                                     | 200mm               | 3   | each  | 5.49            | 16.47      | 10.87      | https://www.aliexpress.com/item/1005007457419235.html             |
| ElectronicModule       | D20L25 Lead Screw Coupler                                               | -                   | 3   | each  | 2.76            | 8.28       | 5.46       | https://www.aliexpress.com/item/1005006456811778.html             |
| Haldis                 | Gearset Kit                                                             | -                   | 1   | each  | 21.39           | 21.39      | 14.12      | https://www.aliexpress.com/item/1005004699143725.html             |
| Lerdge                 | Lerdge iX 180mm Hotbed (Magnetic)                                       | -                   | 1   | each  | 30.79           | 30.79      | 20.32      | https://www.aliexpress.com/item/1005005641707683.html             |
| Good Luck Elec. Prod.  | 2/lot XL4015                                                            |                     | 1   | lot   | 6.21            | 6.21       | 4.10       | https://www.aliexpress.com/item/1005006823558141.html             |
| TLZWLA                 | 10/lot 01x08 2.54mm Female Header Socket                                | -                   | 1   | lot   | 2.16            | 2.16       | 1.43       | https://www.aliexpress.com/item/4001198421663.html                |
|                        | 10/lot 01x20 2.54mm Female Header Socket                                | -                   | 1   | lot   | 2.62            | 2.62       | 1.73       |                                                                   |
| Unnamed                | GY-291 ADXL345 Module                                                   | -                   | 1   | each  | 2.91            | 2.91       | 1.92       | https://www.aliexpress.com/item/1005007557329503.html             |
| ICGOGO                 | 40/lot F-F DuPont Jumper Wires                                          | 100mm               | 1   | lot   | 4.20            | 4.20       | 2.77       | https://www.aliexpress.com/item/1005002000655439.html             |
| YouKeyi                | 5/lot DRV8825 Module                                                    | -                   | 1   | lot   | 9.99            | 9.99       | 6.59       | https://www.aliexpress.com/item/1005009321177962.html             |
| USBO                   | IEC320 C14 Fused Switch                                                 | -                   | 1   | each  | 13.49           | 13.49      | 8.90       | https://www.aliexpress.com/item/4001315809458.html                |
| Wurth Elektronik       | 860040674004 100uF 50V                                                  | D8xL12mm            | 10  | each  | 0.555           | 5.55       | 3.66       | https://au.mouser.com/ProductDetail/Wurth-Elektronik/860040674004 |
| NINDEJIN NINDEJIN      | 50/lot M2x8mm Hex Wafer Head Screw                                      | -                   | 1   | lot   | 2.06            | 2.06       | 1.36       | https://www.aliexpress.com/item/1005008750192874.html             |
| Don Eden               | Pan Screws (PH)                                                         | 50pcs M3x5mm        | 1   | lot   | 2.82            | 2.82       | 1.86       | https://www.aliexpress.com/item/1005008709978631.html             |
|                        | (note, 16mm screws are in place of 15mm screws due to lack of listings) | 50pcs M3x16mm       | 1   | lot   | 4.29            | 4.29       | 2.83       |                                                                   |
|                        |                                                                         | 50pcs M3x35mm       | 1   | lot   | 6.09            | 6.09       | 4.02       |                                                                   |
|                        |                                                                         | 20pcs M4x8mm        | 1   | lot   | 3.32            | 3.32       | 2.19       |                                                                   |
|                        |                                                                         | 10pcs M5x8mm        | 7   | lot   | 3.32            | 23.24      | 15.34      |                                                                   |
|                        |                                                                         | 10pcs M5x16mm       | 2   | lot   | 3.90            | 7.80       | 5.15       |                                                                   |
|                        | Countersunk Screws                                                      | 20pcs M4x5mm        | 1   | lot   | 3.74            | 3.74       | 2.47       |                                                                   |
| Hundred Years          | Pan Screws (PH)                                                         | 50pcs M3x8mm        | 1   | lot   | 2.64            | 2.64       | 1.74       | https://www.aliexpress.com/item/1005006674754845.html             |
|                        |                                                                         | 50pcs M3x10mm       | 1   | lot   | 2.73            | 2.73       | 1.80       |                                                                   |
|                        |                                                                         | 50pcs M3x20mm       | 1   | lot   | 3.55            | 3.55       | 2.34       |                                                                   |
|                        |                                                                         | 50pcs M3x25mm       | 1   | lot   | 3.89            | 3.89       | 2.57       |                                                                   |
|                        |                                                                         | 50pcs M8x50mm       | 1   | lot   | 8.02            | 8.02       | 5.29       |                                                                   |
|                        | Heated Inserts                                                          | 100pcs M2L2 OD3.2mm | 1   | lot   | 2.89            | 2.89       | 1.91       | https://www.aliexpress.com/item/1005006967339727.html             |
|                        |                                                                         | 100pcs M3L4 OD4.2mm | 1   | lot   | 2.35            | 2.35       | 1.55       |                                                                   |
| CANOT                  | Hex Nuts                                                                | 50pcs M3            | 1   | lot   | 2.19            | 2.19       | 1.45       | https://www.aliexpress.com/item/1005007593861199.html             |
|                        |                                                                         | 10pcs M8            | 1   | lot   | 3.00            | 3.00       | 1.98       |                                                                   |
| RTLECS                 | 5/lot 8P 2.54mm Pogo Pins                                               | -                   | 1   | lot   | 11.59           | 11.59      | 7.65       | https://www.aliexpress.com/item/4001036140528.html                |
| MEAN WELL              | LRS-350-24                                                              | -                   | 1   | each  | 55.22           | 55.22      | 36.45      | https://au.mouser.com/ProductDetail/709-LRS350-24                 |
| FreeBoom               | PET Expandable Cable Sleeve                                             | 25mmx2m             | 1   | each  | 11.09           | 11.09      | 7.32       | https://www.aliexpress.com/item/1005009088606787.html             |
| Unnamed                | 100/lot M/F Spade Connectors                                            | 16-14AWG            | 1   | lot   | 5.61            | 5.61       | 3.70       | https://www.aliexpress.com/item/1005009138598203.html             |
| Unnamed                | Black Copper Cable                                                      | 5m, 22AWG           | 1   | lot   | 3.01            | 3.01       | 1.99       | https://www.aliexpress.com/item/1005006647928006.html             |
|                        |                                                                         | 2m, 16AWG           | 1   | lot   | 3.68            | 3.68       | 2.43       |                                                                   |
| PeoPoly                | Magneto X Lancer Melt Zone Long                                         | -                   | 1   | each  | 45.44           | 45.44      | 29.99      |                                                                   |
| Lerdge                 | PEI Bed                                                                 | 180x180             | 1   | each  | 11.79           | 11.79      | 7.78       | https://www.aliexpress.com/item/1005005332775787.html             |
| wuhushiyu              | T-Nuts                                                                  | M5 / 20 Series      | 150 | each  | 0.0676          | 10.14      | 6.69       | https://www.aliexpress.com/item/32814359094.html                  |
|                        |                                                                         | M3 / 20 Series      | 50  | each  | 0.0782          | 3.91       | 2.58       |                                                                   |
| Raspberry Pi           | Pi 4B (out of stock, cannot verify pricing details)                     | -                   | 1   | each  |                 | 0          | 0.00       |                                                                   |
|                        | Pi Pico H                                                               | -                   | 1   | each  | 8               | 8          | 5.28       | https://au.mouser.com/ProductDetail/Raspberry-Pi/SC0917           |
| WGXCPP                 | 127/lot Heat Shrink Kit                                                 | -                   | 1   | kit   | 4.09            | 4.09       | 2.70       | https://www.aliexpress.com/item/1005001787291963.html             |
| ?                      | microSD Card (self sourced)                                             | -                   | 2   | each  |                 | 0          | 0.00       |                                                                   |
| Tojiato                | 4/lot GT2 Idlers W6B5                                                   | 20T                 | 2   | lot   | 5.89            | 11.78      | 7.77       | https://www.aliexpress.com/item/1005007557987612.html             |
|                        |                                                                         | 20T Smooth          | 1   | lot   | 5.92            | 5.92       | 3.91       |                                                                   |
| Maecoom                | 3/lot GT2 Timing Pulley W6B5                                            | 20T                 | 1   | lot   | 6.55            | 6.55       | 4.32       | https://www.aliexpress.com/item/1005003176136280.html             |
| DFORCE Trianglelab     | 6mm Timing Belt                                                         | 3000mm              | 1   | each  | 19.11           | 19.11      | 12.61      | https://www.aliexpress.com/item/1005006507781085.html             |
| Panda Bearings         | 2/lot LM8UU Bearings                                                    | -                   | 2   | lot   | 3.73            | 7.46       | 4.92       | https://www.aliexpress.com/item/1005007070280422.html             |
| [PCB] (5/lot) {JLCPCB} | Supp. Board                                                             | -                   | 1   | lot   | 10.62           | 10.62      | 7.01       |                                                                   |
|                        | Male T-Plug                                                             | -                   | 1   | lot   | 3.21            | 3.21       | 2.12       |                                                                   |
|                        | Female T-Plug                                                           | -                   | 1   | lot   | 3.21            | 3.21       | 2.12       |                                                                   |
|                        | ADXL Connector                                                          | -                   | 1   | lot   | 3.21            | 3.21       | 2.12       |                                                                   |
| NEWHONGHUIDA Fastener  | 30/lot Dowel Pins                                                       | M5x20mm             | 1   | lot   | 7.38            | 7.38       | 4.87       | https://www.aliexpress.com/item/4000473863693.html                |
| excellence             | 20/lot JST PH2.0 8P Connector                                           | Horizontal          | 1   | lot   | 3.16            | 3.16       | 2.09       | https://www.aliexpress.com/item/1005007755047389.html             |
|                        |                                                                         | Vertical            | 1   | lot   | 3.10            | 3.10       | 2.05       |                                                                   |
| Unnamed                | 5/lot PH 8P Ribbon Connector (Single Head)                              | 800mm               | 2   | lot   | 8.39            | 16.78      | 11.07      | https://www.aliexpress.com/item/1005006460578382.html             |
| SVALID                 | 10/lot 4P 24AWG JST XH-2.54 Cable                                       | 150mm               | 1   | lot   | 4.19            | 4.19       | 2.77       | https://www.aliexpress.com/item/1005002376525415.html             |
| alinsin                | 10/lot KF120 2.54mm Terminal Block                                      | 4P                  | 1   | lot   | 4.42            | 4.42       | 2.92       | https://www.aliexpress.com/item/1005003179482974.html             |
|                        |                                                                         | 3P                  | 1   | lot   | 3.47            | 3.47       | 2.29       |                                                                   |
| Creality               | CR-Touch ABL (non-bracket)                                              | -                   | 1   | kit   | 38.79           | 38.79      | 25.60      | https://www.aliexpress.com/item/1005009104612536.html             |
| [Filament]             | 1kg PETG Black (self sourced)                                           |                     |     |       |                 | 0          | 0          |                                                                   |
|                        | 1kg PETG Pink (self sourced)                                            |                     |     |       |                 | 0          | 0          |                                                                   |
|                        |                                                                         |                     |     |       | Shipping        | 50.77      | 33.51      |                                                                   |
|                        |                                                                         |                     |     |       | Subtotal        | 922.93     | 609.13     |                                                                   |
|                        |                                                                         |                     |     |       | +10% GST        | 92.29      | 60.91      |                                                                   |
|                        |                                                                         |                     |     |       | Total           | 1015.22    | 670.05     |                                                                   |
|                        |                                                                         |                     |     |       | Hack Club Grant | 530.30     | 350.00     |                                                                   |
|                        |                                                                         |                     |     |       | Out Of Pocket   | 484.91     | 320.05     |                                                                   |
