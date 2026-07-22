# Keyboards

> TODO: verify remaining details. Core USB limitation confirmed below.

## Connector / interface

- **USB only — and specifically USB 1.1 (USB1), not USB 2.0/3.0.** This significantly narrows the pool of compatible keyboards. Modern USB 2.0/3.0-only keyboards may not be recognized.
- TODO: confirm exact USB host chip/limitation causing this (hardware or firmware constraint?)
- TODO: confirm connector type (USB-A? micro/USB-C with a USB1-speed host controller?)

## Practical buying guidance

- **Old USB1-era keyboards are the safe bet.** Keyboards from the early USB transition period (roughly late 1990s–early 2000s) are far more likely to negotiate at USB1 (full-speed/low-speed) rather than requiring USB2+.
- It's not a hard rule, though — compatibility has been hit-or-miss across both old and modern keyboards in testing so far (see tables below). When in doubt, test before relying on a keyboard.

## Tested & known-working

| Keyboard | Interface | Notes |
|---|---|---|
| Logitech K120 | USB1 | Confirmed working. The unit tested had a Spanish key layout, which made locating some keys difficult — a layout/labeling issue, not a compatibility one. |
| Perixx Periboard-517 | USB1 | Confirmed working. |
| Ziyoulang K61 RGB | USB1 | Confirmed working, reported as "a bit hokey" (exact meaning unclear — possibly minor quirks in feel/behavior). |
| Acer Model OM-130006A/K | USB1 | Confirmed working. |
| HP PN: 803181-001 US | USB1 | Confirmed working. |

## Known NOT to work

| Keyboard | Notes |
|---|---|
| Dell SK-8135 | Not recognized. |
| Digital Innovations model 4250500 | Not recognized. |
| Royal Kludge RK84 | Not recognized. |
| Epomaker/Skyloong SK64 | Not recognized. |
| Case Logic Mini Keyboard (KD-300) | Connects and is recognized, but produces random characters — unusable. |
| Cherry Stream Keyboard TKL — Model JK-85TKL | Not recognized. |
| Keychron K14 Wireless | Not recognized. Wireless (dongle/Bluetooth) — failure may be specific to that connection method rather than the keyboard's USB HID compatibility in general. |

## Original CoCo/Tandy keyboards

- TODO: can an original CoCo 2/3 keyboard be wired directly to the device? If so, pinout/adapter needed.

## Key mapping

- See [keyboard-shortcuts.md](../02-menus-and-shortcuts/keyboard-shortcuts.md) for CoCo-specific key mapping.

## Case entry note

- Text entry defaults to uppercase. Hold **LEFT SHIFT** to type lowercase (e.g. when entering a mixed-case WiFi password) — see [modem-menu.md](../02-menus-and-shortcuts/modem-menu.md).
