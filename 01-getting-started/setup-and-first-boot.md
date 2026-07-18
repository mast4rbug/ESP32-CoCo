# Setup & First Boot

## In the box / what you need

- **The box contains only the ESP32-COCO device itself**, in a 3D-printed case.
- **Nothing else is required for the device to boot.** No SD card is needed just to power it on.
- You'll need to supply: a USB power source/cable, a video cable, and eventually a keyboard, SD card, and display — see [Connecting peripherals](#connecting-peripherals) below.

## First power-on

1. Connect USB power (micro-USB, ~0.5A — see [hardware-specs.md](hardware-specs.md)) and a video cable (VGA, or HDMI on newer boards).
2. The device boots right up — **no SD card required** just to reach the CoCo screen.
3. TODO: what a successful first boot looks/sounds like (boot screen details, LED behavior — see [hardware-specs.md](hardware-specs.md) for the LED indicator)

## Preparing an SD card

An SD card isn't required to boot, but you do need one for two things: **saving any configuration made in the F12 menu** (settings don't persist without it) and **loading/saving any programs** (disks, cassettes, etc.).

- **FAT32 required.**
- No specific folder structure is required — see [sd-card.md](sd-card.md) for details.
- No SD card is needed just to boot the device.

## Connecting peripherals

- Keyboard — see [keyboards.md](../03-compatible-hardware/keyboards.md)
- Joystick — see [joysticks-and-controllers.md](../03-compatible-hardware/joysticks-and-controllers.md)
- Display — VGA on all boards, HDMI on newer boards; see [hardware-specs.md](hardware-specs.md)

## Verifying it works

- TODO: quick smoke test (e.g. load a known-good DSK/WAV file) — see [Disk Menu](../02-menus-and-shortcuts/disk-menu.md) and [Cassette Menu](../02-menus-and-shortcuts/cassette-menu.md)

## If something goes wrong

- See [Troubleshooting](../04-management/troubleshooting.md)
