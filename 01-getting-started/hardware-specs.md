# Hardware Specs

> Confirmed via community/maintainer knowledge (2026-07-08). Still TODO: full revision history — flag corrections as they come in.

## Core

| Component | Spec |
|---|---|
| SoC | ESP32-S3-WROOM-1 |
| Flash | 8 MB |
| PSRAM | 8 MB |
| Internal fast RAM | 384 KB (on-chip SRAM) |
| Emulated CoCo RAM | 2 MB (device emulates a CoCo 3 with 2 MB of RAM) |
| Storage | Standard SD card, **FAT32 required** |

## Video output

- **VGA** on all boards.
- Some newer boards also offer **HDMI**, but HDMI output is reported **less stable than VGA** — VGA is the safer choice if given the option.

## Audio output

- 3.5 mm (1/8") jack, **mono**.

## Input

- **Keyboard**: USB, and specifically **USB 1.1 (USB1) only** — not USB2/3. See [keyboards.md](../03-compatible-hardware/keyboards.md).
- **Joysticks**: 2× USB1 ports, supports both analog pads and digital controllers. See [joysticks-and-controllers.md](../03-compatible-hardware/joysticks-and-controllers.md).

## Expansion port

- A side-mounted expansion port accepts an **optional joystick module** that lets you connect standard/original CoCo joysticks directly (as an alternative to USB).

## Serial port

- 3.5 mm (1/8") jack, wired as **TRS (tip/ring/sleeve)**: Tip = Receive Data From Other, Ring = Send Data To Other, Sleeve = GND.
- Used for the RS-232 PAK hardware serial feature and the WiFi/Telnet bridge — see [modem-menu.md](../02-menus-and-shortcuts/modem-menu.md), which also has the pinout diagram and cable-building notes.

## Cassette port

- Two 3.5 mm (1/8") jacks: **CAS** and **CTL** (relay). **CAS is bidirectional** — it carries both cassette in (loading) and cassette out (saving), unlike separate mono in/out jacks on some real tape decks.
- To connect a real CoCo tape deck (which has separate mono in/out jacks), you'll need a **1/8" stereo-to-mono Y-splitter cable** to break the bidirectional CAS signal out into separate in/out connections.
- **CTL** is a simple mono signal — just a plain **1/8" mono-to-mono cable**, end to end, no splitter needed.
- See [cassette-menu.md](../02-menus-and-shortcuts/cassette-menu.md) for loading/saving programs via this port.

## LED indicator

- Single front LED: **red** = power on, **flashes green** = disk activity.

## Power

- **Micro-USB** input, draws roughly **0.5 A**.

## Physical

- Ships in a **3D-printed case** or as a naked board
- Board dimensions: **4 × 3 inches**.
- Box contents: **the device only** — see [setup-and-first-boot.md](setup-and-first-boot.md). No SD card, cables, or peripherals included.

## Revisions

| Board revision | Notes |
|---|---|
| V1.2 | VGA version |
| V1.3 | HDMI + Option port (for joystick module) |

- TODO: track hardware revisions here as more are confirmed
