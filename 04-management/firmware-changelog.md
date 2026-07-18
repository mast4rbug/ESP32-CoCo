# Firmware Changelog

Version history for ESP32-COCO device firmware. For how to actually flash a `.FLH` file, see [firmware-upgrade-menu.md](../02-menus-and-shortcuts/firmware-upgrade-menu.md).

> Ordering note: versions are listed newest-first based on feature accumulation (V1.04 includes capabilities not present in V1.0.2's notes). TODO: confirm exact version numbering/order and whether "V1.04" is shorthand for "V1.0.4", plus fill in any versions between/before/after these.
> **Current published firmware download:** https://drive.google.com/file/d/1Avexaa-GsFraal4dFbb2e44r8fiGZH3m/view
> **V1.05 exists but is not yet published.** Confirmed by the creator — it ships on the newest board revision, but there's no public download or release notes for it yet.
> **Going forward, firmware may fork per board revision.** There are two board revisions (V1.2, V1.3 — see [hardware-specs.md](../01-getting-started/hardware-specs.md)), and V1.3 has additional hardware (HDMI, expansion/option port). Future firmware releases are expected to be built per-revision, disabling features the older V1.2 board can't physically support.

## V1.04 — Board Revision V1.2

- Added hardware and software revision display in the menu.
- Added **F9** to save a screenshot — saved to SD card root as incremental `PICTUREXXXX.BMP`.
- Added **Save State** (F3) and **Load State** (F4) — save/load game or work progress, or use for fast-loading. 36 slots available (0–9, A–Z).
- Added Disk menu option to create a new, formatted `.DSK` file.
- Added Disk menu **FORMAT** option to format an existing `.DSK` file.
- Added **DEL** key to remove/eject a disk from any drive (0–3).

## V1.0.2 — Board Revision V1.2

File: `CC3-BOARDV1-2-FW1-0-2.FLH`
Download: https://drive.google.com/file/d/1Avexaa-GsFraal4dFbb2e44r8fiGZH3m/view

**Flashing instructions:** copy the file to the root of the SD card, then flash it via the Flash Firmware menu (**F12**).

**Changes:**

- Fixed file corruption issue when saving to disk.
- Fixed screen centering (was shifted too far right).
- Fixed display bug when loading from cassette.
- Added **F10** to toggle between artifact modes (BLUE-RED / RED-BLUE).
- Added Vsync enable/disable (better compatibility with Twilight Terminal, less flickering).
- Added RS-232-PAK modem support via the hardware serial port.
- Added RS-232-PAK ↔ WiFi bridge for Telnet BBS connections.
- Added **F11** to exit data mode and return to command mode (WiFi mode only).
- Fixed various minor bugs.

See [modem-menu.md](../02-menus-and-shortcuts/modem-menu.md) for full detail on the RS-232/WiFi features this version introduced.

## Earlier versions

- TODO: no earlier firmware versions documented yet.
