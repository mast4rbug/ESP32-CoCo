# Joysticks & Controllers

## Connector / interface

- **2× USB ports, USB Low Speed (1.5 Mbps) only** — not Full Speed (12 Mbps, most of USB 1.1) or High Speed (480 Mbps, USB 2.0+). Same constraint as keyboards — see [keyboards.md](keyboards.md#connector--interface) for the technical explanation and a possible ADuM4160-adapter workaround. This rules out most modern USB gamepads, which is why the community compiles confirmed-working controllers (often older/legacy models, or cheap ones from AliExpress) below.
- Supports both **analog pads and digital controllers**.
- An **expansion port** on the side of the board accepts an optional joystick module that connects **standard/original CoCo joysticks** directly, bypassing USB entirely — see [hardware-specs.md](../01-getting-started/hardware-specs.md).
- TODO: is any digital-to-analog mapping done internally for CoCo-style analog joystick emulation, or is it 1:1 passthrough for analog pads?

## Known-working (community-sourced)

| Controller                                                               | Source            | Link                                                                                                                                    | Notes                                                                                               |
| ------------------------------------------------------------------------ | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Unnamed USB joystick                                                     | AliExpress        | https://www.aliexpress.com/item/1005010597048106.html                                                                                   | Reported working. TODO: confirm product name/model — AliExpress listings can change or be delisted. |
| Logitech RumblePad 2                                                     | Legacy/secondhand | P/N 863247-0000 (no link — legacy device, check eBay/thrift)                                                                            | Reported working.                                                                                   |
| Logitech Wingman Action Pad                                              | Legacy/secondhand | Model 963247-0914, also part number G-UB3A (no link — legacy device)                                                                    | Reported working.                                                                                   |
| Rii Game Controller (Retro USB Controller)                               | Amazon            | https://www.amazon.com/dp/B073Z9MKKH                                                                                                    | Reported working.                                                                                   |
| USB SNES-style joypad ("Controller Classic Nintendo Computer Raspberry") | Amazon            | CA: https://www.amazon.ca/-/fr/dp/B075QJKBLV · US: https://www.amazon.com/Controller-Classic-Nintendo-Computer-Raspberry/dp/B075QJKBLV/ | Reported working.                                                                                   |
| Hyperkin "Scout" Premium USB Controller (PC/Mac)                         | Amazon            | https://www.amazon.com/dp/B0798GFM6V                                                                                                    | Reported working.                                                                                   |

## Buying guidance

- When shopping AliExpress/Amazon/secondhand for a compatible controller, older/basic USB gamepads are far more likely to negotiate at USB1 than modern USB2+ controllers — there's no reliable way to tell from a listing alone besides community reports, so treat the table above as the source of truth as it grows.
- A [Joystick Config Editor by Mike Horgan](../05-resources/utilities.md) is available to help set up a controller once connected.
- A [joystick testing .DSK image](../05-resources/media-library.md) from the creator is available to verify a controller works correctly.

## Tested & known-NOT-working

| Controller | Notes |
|---|---|
| TODO | TODO |

## Original CoCo joysticks

- Supported via the optional expansion-port joystick module — see [hardware-specs.md](../01-getting-started/hardware-specs.md). No adapter needed when using that module; not connected via USB.

## Number of ports

- 2 USB Low Speed joystick ports (2-player support via USB), plus the expansion port for original CoCo joysticks.

## See also

- [Joystick Menu](../02-menus-and-shortcuts/joystick-menu.md) — configuring axes/buttons on-device (including the axis-number gotcha)
