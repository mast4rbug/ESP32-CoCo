# Overview

## What it is

ESP32-COCO is a bare-metal hardware emulator for the Tandy/Radio Shack TRS-80 Color Computer 1-2 and Color Computer 3, running on ESP32-S3. Created by Cedric Beaudoin.

**What's an ESP32?** The ESP32-S3 is a small, inexpensive microcontroller chip — normally used in low-power embedded projects like smart-home gadgets, not for emulating a whole computer. The "32" in its name refers to it being a 32-bit chip, and has nothing to do with the CoCo's own "32K" memory configurations from the 1980s — ESP32-COCO isn't emulating a stock 32K CoCo. The ESP32-S3 that powers this device has enough processing power and memory to emulate a full CoCo 3, including its emulated **2 MB of RAM** — far beyond what any real CoCo 3 ever shipped with.

ESP32-COCO is aimed at retro computing hobbyists. Real CoCo 3 hardware is scarce, and the GIME chip at its heart is no longer produced, which pushes prices on the collector/hobby market up considerably. ESP32-COCO sidesteps both problems by emulating the GIME chip (and the rest of the CoCo 3) on ESP32-S3 hardware, giving hobbyists a much cheaper way to get CoCo 3 capability. It's also dramatically more compact than a real CoCo 3.

- Compared to software emulators (e.g. VCC, MAME, XRoar), ESP32-COCO runs as firmware on a tiny ESP32-S3, which limits it to what that firmware implements — it can't connect real peripherals through a real or virtual Program Pak expansion. Hardware add-ons like the Orchestra-90, Voice Pak, or real disk controllers aren't possible on ESP32-COCO. Like software emulators, though, it can read simulated disks and cassettes (DSK/WAV files) — see [Disk Menu](../02-menus-and-shortcuts/disk-menu.md) and [Cassette Menu](../02-menus-and-shortcuts/cassette-menu.md).
- **Project maturity:** the hardware itself is considered pretty much final. Further development is expected to come through firmware updates and through the expansion port — see [firmware-changelog.md](../04-management/firmware-changelog.md) for what's shipped so far.
- **How to get one:** there's no official store. Cedric produces the device in batches from time to time and maintains a request list for people interested in buying one — TODO: link to the request list once confirmed.

## What it emulates

- **CPU**: Motorola 68B09.
- **GIME**: the GIME chip is emulated — see [What it is](#what-it-is) above for why this matters (GIME chips are no longer produced).
- **Sound**: the CoCo doesn't have a dedicated sound chip — sound is produced by a simple 6-bit DAC, which ESP32-COCO emulates.
- Emulates a CoCo 3, which is backward compatible with CoCo 1 and CoCo 2 software — there is no separate/explicit CoCo 1 or CoCo 2 mode.

## Who made it / where the project lives

- Creator: Cedric Beaudoin
- Official documentation home: https://github.com/mast4rbug/ESP32-CoCo — also the intended future home for firmware update files and, potentially, device source code.
- TODO: link to community hub — see [community-links.md](../05-resources/community-links.md)

## Documentation status

Before this repo (created 2026-07-08), there was no central GitHub repo, product page, or written manual for ESP32-COCO — most information circulated via the CoCo Facebook community and creator demo videos. This documentation set exists to consolidate that scattered knowledge. Flag and correct anything below that's inaccurate or outdated.
