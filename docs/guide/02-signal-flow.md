# 02. Signal flow

[Start here](00-start-here.md)

## Audio

```mermaid
flowchart LR
  MM[Main M1] -- "USB-C A" --> PA[PlayAUDIO1U]
  BM[Backup M1] -- "USB-C B" --> PA
  PA -- "XLR 1-12" --> XR[XR18]
  XR -- "Aux 1-5" --> IEM[Five IEM transmitters]
  XR -- "Main L/R" --> FOH[Dual snake to FOH]
```

Output 15 is the LifeSine tone and is not patched. [Cable schedule](../cable-schedule.md).

## MIDI

```mermaid
flowchart LR
  PA[PlayAUDIO1U] -- "USB MIDI to both Minis" --> MM[Main]
  PA -- "USB MIDI to both Minis" --> BM[Backup]
  FS[Footswitch] -- "CONTROL port" --> PA
  MM -. "RTP only in record mode" .-> BM
```

Perform mode keeps Mini-to-Mini RTP off or unrouted. [RTP-MIDI setup](../rtp-midi-setup.md).

## Network

```mermaid
flowchart LR
  SW["Switch, no DHCP"]
  MM["Main 192.168.1.11"] --- SW
  BM["Backup 192.168.1.12"] --- SW
  PA["PlayAUDIO1U .13"] --- SW
  XR["XR18 .20"] --- SW
  TAB["Tablets .51 to .55"] --- SW
```

[Network plan](../network-and-ip-plan.md).

## Video

```mermaid
flowchart LR
  MM[Main HDMI] -- "input 1" --> HSV[2-in/1-out HDMI switch]
  BM[Backup HDMI] -- "input 2" --> HSV
  HSV --> SPL[1x2 splitter]
  SPL -- "HDBaseT" --> PROJ[Two projectors]
```

A 2x2 matrix can replace the switch-plus-splitter if each screen must be picked alone. No model is chosen. [Video](../video-projectors.md).

## Lighting

```mermaid
flowchart LR
  MM[Main Mini Lightkey] -- "USB-A" --> ENT[Enttec]
  ENT -- "DMX 5-pin" --> FIX[Fixtures]
```

[Lighting](../lighting-lightkey.md).

## Power

The Furman M-8x2 feeds the main case. One extension lead from the Furman feeds a small strip in the control case. The plan does not publish a manufacturer power-on order. The [show-day runbook](../../SHOW-DAY-RUNBOOK.md) uses Furman, switch, PlayAUDIO1U, Minis, XR18, IEMs, then control and projectors, and says that sequence is unverified as a manual.
