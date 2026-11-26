# 05. Failover

[Start here](00-start-here.md)

## What switches

The PlayAUDIO1U listens for a LifeSine test tone on output 15 from the Main Mini. A blinking shield means the tone is armed. Pulling the USB cable from DAW A should move audio and MIDI to the Backup on DAW B without a gap. Scene A is the normal scene. [Cases](../cases-and-rack-layout.md).

A footswitch on a CONTROL port, assigned in Auracle X, or the touch panel, switches by hand. [Auracle X](https://www.iconnectivity.com/auracle-x-series).

## Keeping the Minis identical

Same Live set, same samples, same sample rate, same output routing. AbleSet on both, AbleNet on, drift correction on the backup only, all clips warped. [AbleNet](https://ableset.app/docs/ablenet).

**Unverified:** a file-sync product. Copy the set by whatever means you trust, then open it on both Minis and read the set name before doors. [Show-day runbook](../../SHOW-DAY-RUNBOOK.md).

## What does not follow automatically

- Lightkey’s license is one Mac at a time. Moving it is slow. A USB-DMX interface with its own processor holds the last look. [Lighting](../lighting-lightkey.md).
- A Mac that has crashed can still output HDMI, so the 2-in/1-out HDMI switch may not change by itself. Select input 2 by hand. [Video](../video-projectors.md).
- Mini-to-Mini RTP stays off in perform mode so transport commands are not doubled. [RTP-MIDI setup](../rtp-midi-setup.md).

## After a switch

Use Sync Playback Now so the playhead matches. [AbleNet](https://ableset.app/docs/ablenet). Put DAW A back and confirm Scene A before the next song if the Main Mini is healthy.
