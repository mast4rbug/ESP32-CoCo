# Keyboards

## Connector / interface

- **USB Low Speed (1.5 Mbps) only** — the actual constraint is narrower than "USB 1.1" alone suggests. ESP32-COCO uses a USB "Soft Host" library that can only handle **Low Speed (1.5 Mbps)** devices, not **Full Speed (12 Mbps)** — most USB 1.1 peripherals — or **High Speed (480 Mbps)**, i.e. USB 2.0+. This is why compatibility has been hit-or-miss even among older USB 1.1 keyboards: being "USB 1.1" doesn't guarantee it negotiates at Low Speed. (Source: Cedric, via discussion with Rocco Corsi on the CoCo Discord's #esp32-coco channel.)
- **Connector type: classic USB-A ports.**

## Practical buying guidance

- **Old USB1-era keyboards are the safer bet, but it's not a guarantee** — compatibility has been hit-or-miss across both old and modern keyboards in testing so far (see tables below), since the real requirement is Low Speed negotiation specifically, not just "USB 1.1." When in doubt, test before relying on a keyboard.
- **Workaround for Full Speed (12 Mbps) devices:** a USB isolator adapter built around the **ADuM4160** chip, specifically one with a **1.5 Mbps / 12 Mbps speed-lock switch**, can force a Full Speed device down to Low Speed and make some otherwise-incompatible keyboards/joysticks work. It won't help High Speed (480 Mbps, USB 2.0+) devices. Factor the adapter's cost into the decision — it may be cheaper to just try a different keyboard. Anecdotally (Rocco Corsi, same Discord discussion): of 5 keyboards tested, 3 worked natively, 1 worked only with the ADUM4160 switch set to 1.5 Mbps, and 1 didn't work even with the adapter.

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

## Key mapping

- See [keyboard-shortcuts.md](../02-menus-and-shortcuts/keyboard-shortcuts.md) for CoCo-specific key mapping.

## Case entry note

- Text entry defaults to uppercase. Hold **LEFT SHIFT** to type lowercase (e.g. when entering a mixed-case WiFi password) — see [modem-menu.md](../02-menus-and-shortcuts/modem-menu.md).
