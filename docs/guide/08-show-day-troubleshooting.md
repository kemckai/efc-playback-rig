# 08. Show-day troubleshooting

[Start here](00-start-here.md)

Use the one-line table in the [show-day runbook](../../SHOW-DAY-RUNBOOK.md) first. This chapter is the longer version of those lines. Steps that are not in a manual are marked.

## No audio

Confirm Scene A, both USB-C DAW cables, and the blinking LifeSine shield. Then XR18 scene PERFORM and Main L/R on the snake. Click must not be the only thing you hear in the house. [Modes](../modes-and-checklists.md).

## Failover already happened

Leave the Backup playing. Sync Playback Now. Do not move the Lightkey license during a song. Select HDMI input 2 if the projectors stayed on a dead Main picture. [Failover](05-failover.md).

## MIDI not syncing

Perform mode: Mini-to-Mini RTP should be off or unrouted, Link off, AbleNet on. Record mode is the opposite for RTP and Link. [RTP-MIDI setup](../rtp-midi-setup.md).

If AbleNet does not see the other Mini, enter `192.168.1.11` and `192.168.1.12` under Connect to Custom IPs. [AbleNet](https://ableset.app/docs/ablenet).

## Tablet disconnected

Check the Ethernet adapter and the switch link light. Open the other Mini’s address from the AbleSet menu-bar window. **Unverified:** the web port. [ableset.md](../ableset.md).

## Projector, no signal

The path is HDMI switch, then 1x2 splitter, then HDBaseT. It is not the KVM. A crashed app can still output a picture, so change the switch by hand. [Video](../video-projectors.md).

## IEM dropouts and RF

Scan with the transmitter maker’s tool. Five channels need a coordinated set. Do not operate in 617–652 MHz or 663–698 MHz. One player can use the PlayAUDIO1U headphone output as a click backup. [IEM mixes](../iem-mixes.md).

**Unverified:** which IEM product is packed, and any guitar wireless (GLXD16+ or Relay G10SII are only under consideration).
