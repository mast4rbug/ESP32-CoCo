# Keyboards

> TODO: verify remaining details. Core USB limitation confirmed below.

## Connector / interface

- **USB only — and specifically USB 1.1 (USB1), not USB 2.0/3.0.** This significantly narrows the pool of compatible keyboards. Modern USB 2.0/3.0-only keyboards may not be recognized.
- TODO: confirm exact USB host chip/limitation causing this (hardware or firmware constraint?)
- TODO: confirm connector type (USB-A? micro/USB-C with a USB1-speed host controller?)

## Practical buying guidance

- **Old USB1-era keyboards are the safe bet.** Keyboards from the early USB transition period (roughly late 1990s–early 2000s) are far more likely to negotiate at USB1 (full-speed/low-speed) rather than requiring USB2+.
- TODO: note any modern keyboards confirmed to still work (some cheap/basic USB keyboards still ship as USB1-compatible)
- TODO: note any keyboards confirmed NOT to work

## Tested & known-working

| Keyboard | Interface | Notes |
|---|---|---|
| TODO | USB1 | TODO |

## Original CoCo/Tandy keyboards

- TODO: can an original CoCo 2/3 keyboard be wired directly to the device? If so, pinout/adapter needed.

## USB keyboards

- TODO: general USB HID keyboard compatibility notes
- TODO: any keyboards known NOT to work

## Key mapping

- See [keyboard-shortcuts.md](../02-menus-and-shortcuts/keyboard-shortcuts.md) for CoCo-specific key mapping.

## Case entry note

- Text entry defaults to uppercase. Hold **LEFT SHIFT** to type lowercase (e.g. when entering a mixed-case WiFi password) — see [modem-menu.md](../02-menus-and-shortcuts/modem-menu.md).
