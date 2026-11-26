# Cable schedule

[Eugene Fight Club playback rig](../README.md)

Perform mode.

The PlayAUDIO1U's two USB-C DAW ports are on the front panel. The rear has only AC, the power switch, 12 XLR outputs and the RTP-MIDI Ethernet port. There is no rear USB. Two USB-C to USB-C cables come in the box. Keith's front USB-A host port is broken: do not use it.

| From | To | Cable | Note |
| --- | --- | --- | --- |
| Main Mini USB-C | PlayAUDIO1U front USB-C A | USB-C to USB-C (2 in the box) | Computer A. Carries audio and MIDI. |
| Backup Mini USB-C | PlayAUDIO1U front USB-C B | USB-C to USB-C (2 in the box) | Computer B. Same session loaded. |
| PlayAUDIO1U XLR out 1-12 | XR18 inputs (via I/O panel) | XLR male to XLR male jumpers | Suggested map below. Leave output 15 for the control tone (internal). |
| XR18 Aux 1-5 XLR | IEM transmitter inputs | XLR | One mono mix per player. |
| XR18 Main L/R XLR | Dual snake | XLR | To FOH. |
| Both Minis Ethernet | Gigabit switch | Cat5e or Cat6 | AbleNet, RTP-MIDI, Lightkey, tablets. |
| XR18 Ethernet | Gigabit switch | Cat5e or Cat6 | Set REMOTE switch to Ethernet. |
| Wired tablets | Gigabit switch | Ethernet adapter (owned) | AbleSet web app and X AIR app. |
| Footswitch | PlayAUDIO1U CONTROL port | 1/4 in TRS | Manual failover. Configure the port in Auracle X. |
| Controller (if any) | PlayAUDIO1U 5-pin DIN MIDI in, or a Mini | MIDI DIN or USB | Do not use the front USB-A host port (broken). |
| Main Mini USB or switch | DMX interface or sACN node | USB or Ethernet | See [Lighting (Lightkey)](lighting-lightkey.md). |
| Each Mini 2x HDMI | 2x1 HDBaseT switchers | HDMI | Never through the KVM. See [Video (projectors)](video-projectors.md). |
| Control case | Each Mini | USB-C (passive 2 m or active optical longer) | One per Mini. Video, keyboard and mouse in one cable. |

The dual snake is assumed to carry XR18 mains and spare channels to FOH. Confirm channel count and whether it is send and return. Using a spare snake channel for DMX is a possible shortcut but was not verified; prefer a separate DMX run (see Lighting).

## Suggested output map

| Out | Suggested use |
| --- | --- |
| 1 | Click (to XR18 channel, aux sends only, not main) |
| 2 | Guide / cues (aux only) |
| 3-4 | Backing stems L/R |
| 5-6 | Drum/percussion stems L/R |
| 7-8 | Synth/bass stems L/R |
| 9-10 | FX/ambience L/R |
| 11-12 | Spare (video audio or SMPTE-style tone if needed) |

This map is a starting suggestion, not from a manual. It leaves four XR18 mic/line inputs for live sources if all 12 outputs are patched; trim it if you need more. Leave output 15 for the control tone (internal).

## Control-case USB-C runs

Passive full-featured USB-C cables are reliable at 2 m for 4K60 DP Alt Mode. For longer runs use an active optical USB-C cable: ACT lists 10 m (up to 15 m) and ADTECHNO lists 7 m and 10 m, both 4K60 DP Alt Mode. Prices unknown.

ADTECHNO marks Source and Display ends. Plug the Mini end into the Source end.

Run one extension lead from the main case's Furman to a small strip in the control case for the monitor and any KVM power.

## Audio path

```mermaid
flowchart LR
  MM[Main Mini] -- "front USB-C A, audio + MIDI" --> PA[PlayAUDIO1U]
  BM[Backup Mini] -- "front USB-C B, audio + MIDI" --> PA
  PA -- "XLR out 1-12 via I/O panel" --> XR[XR18]
  XR -- "Aux 1-5 XLR" --> IEM[IEM transmitter inputs]
  XR -- "Main L/R XLR" --> SN[Dual snake to FOH]
  FS[Footswitch] -- "1/4 in TRS CONTROL port" --> PA
```

Both Minis connect at once in perform mode. Main Mini to DAW A, Backup Mini to DAW B. Scene A should be the active scene.

## Open items

- Dual snake channel count, and whether it is send and return: not confirmed.
- Output map: a starting suggestion, not from a manual.
- DMX on a spare snake channel: not verified.
- Active optical USB-C prices: unknown. Cable, XLR jumper, USB-C and Cat6A prices: unknown.
- Penn Elcom USB-C and HDMI feedthroughs: unverified (see [Cases and rack layout](cases-and-rack-layout.md)).

## Sources

- [PlayAUDIO1U product page](https://www.iconnectivity.com/playaudio1u) (iConnectivity)
- [PlayAUDIO1U user guide](https://www.bhphotovideo.com/lit_files/1048735.pdf) (B&H)
- [Redundant playback rig with PlayAUDIO1U](https://www.iconnectivity.com/blog/creating-a-redundant-playback-rig-with-playaudio1u) (iConnectivity)
- [ACT 10 m USB-C active optical cable](https://www.act-connectivity.com/en-us/products/cables/usb/usb-c-aoc-for-touch-panel-60w-4-lane-10m-ak4330) (ACT)
- [XR18 user manual](https://mediadl.musictribe.com/media/PLM/data/docs/X-AIR/M_BE_0605-AAA_X-AIR_EN.pdf) (Behringer)
