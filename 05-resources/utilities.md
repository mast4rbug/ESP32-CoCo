# Utilities

Tools for building, converting, and managing media files for ESP32-COCO.

## Joystick configuration

| Tool | Purpose | Link | Notes |
|---|---|---|---|
| ESP32-Coco Joystick Config Editor (Mike Horgan) | Configure/edit joystick button and axis mappings | https://gigajunky.github.io/coco/cespcfged.html | **Chromium-based browsers only** (Chrome, Edge, Brave, etc.) — doesn't work in Firefox or Safari. |

See also [joystick-menu.md](../02-menus-and-shortcuts/joystick-menu.md) for the axis-configuration gotcha, and [joysticks-and-controllers.md](../03-compatible-hardware/joysticks-and-controllers.md) for the known-working controller list.

## Cassette conversion tools

| Tool | Purpose | Link |
|---|---|---|
| CAS to WAV Converter (Mike Horgan) | Convert `.CAS` files to `.WAV` (ESP32-COCO only mounts WAV, not CAS) | https://gigajunky.github.io/coco/index.html |

## SD card tools

| Tool | Purpose | Link |
|---|---|---|
| SD Card Formatter (SD Association) | Properly format SD cards to FAT32 for use with the device | https://www.sdcard.org/downloads/formatter/ |
| Remove Dot Files (Floyd Resler) | Removes macOS Finder `._` metadata files that clutter the SD card | https://maccrafters.com/apps/Remove-Dot-Files.zip |

## Disk image tools

| Tool | Purpose | Link |
|---|---|---|
| Coco File Image Utility (Mauricio Matte) | All-around CoCo disk image tool: disk image manipulation, downloading images from FujiNet servers, formatting OS-9 disks, and much more | https://drive.google.com/drive/folders/1jBCOk4TgNj5XINNRegEWGye03VK_T4QT |
| TODO | Create/edit DSK images (note: the device itself can create/format DSK images on-device as of firmware V1.04 — see [disk-menu.md](../02-menus-and-shortcuts/disk-menu.md)) | TODO |

## Firmware flashing tools

- No separate PC tool needed — firmware flashes from a file on the SD card via the device's own F12 menu. Cross-reference: [firmware-upgrade-menu.md](../02-menus-and-shortcuts/firmware-upgrade-menu.md)
