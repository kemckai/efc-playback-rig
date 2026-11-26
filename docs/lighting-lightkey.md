# Lighting (Lightkey)

[Eugene Fight Club playback rig](../README.md)

Lightkey is licensed per Mac, one active at a time, so true lighting redundancy needs two licenses. A free edition outputs 24 channels. The license price is unknown (the store shows US prices).

- Lightkey supports USB-DMX interfaces (Enttec DMX USB Pro and Pro Mk2, DMXking, Eurolite and others) and Art-Net (up to four universes) and sACN. It says it recommends no particular network brand.
- Live Triggers need Ableton Live on the same computer. You drag Lightkey cues onto the Live timeline and they are sent as MIDI on channel 16 to Lightkey Input.
- Lightkey Live Triggers use a local MIDI port on the same Mac, so they need no RTP.
- Lightkey also takes MIDI notes, CC and Program Change, OSC, MIDI Clock, Ableton Link and OS2L.
- One license is active on one Mac at a time. Two Macs controlling lights at once need two licenses. A free edition outputs 24 channels.
- USB interfaces with a built-in microprocessor keep sending the last state when data stops; some low-end ones send zeros and can flicker.
- Recommended: run Lightkey on the Main Mini with an Enttec USB interface. On a Main failure the lights hold their last look; moving the license is slow, so buy a second license only if you need lighting redundancy.
- If you buy two licenses, use an Art-Net or sACN node on the switch and set the backup's DMX output to none until a failover (a design suggestion, not from the docs).
- DMX run: use dedicated DMX cable. Using a spare snake channel is a possible shortcut but was not verified; prefer a separate run.

Enttec DMX USB Pro Mk2: $242.99 (listing price seen Nov 26, 2026). Lightkey supported.

In perform mode, Lightkey and video are on (Main), with projectors connected. In record / studio they are off. The perform checklist includes checking Lightkey output and DMX.

```mermaid
flowchart LR
  MM[Main Mini] -- "USB DMX or sACN" --> DMX[DMX interface/node]
  DMX -- "DMX 5-pin" --> FIX[Fixtures]
```

If a DMX node is used, its address in this plan is 192.168.1.30. Art-Net needs the same subnet. Mask 255.255.255.0. See [Network and IP plan](network-and-ip-plan.md).

The Main Mini reaches the interface by USB, or the switch by Ethernet when the node is sACN or Art-Net. Cable row: Main Mini USB or switch, to the DMX interface or sACN node, USB or Ethernet.

## Open items

- Lightkey license price: unknown (store shows US prices).
- Second license only if lighting redundancy is required. The backup DMX-output-none idea is a design suggestion, not from the docs.
- DMX over a spare snake channel: not verified.
- DMX node is optional. USB-DMX does not need the .30 address.

## Sources

- [Lightkey tech specs](https://www.lightkeyapp.com/en/specs) (Lightkey)
- [Lightkey help and licensing](https://www.lightkeyapp.com/en/help) (Lightkey)
- [Enttec DMX USB Pro Mk2](https://toneloot.com/dj-effects/performance-fx-units/enttec-dmx-usb-pro-mk2-dmx-interface) (ToneLoot)
