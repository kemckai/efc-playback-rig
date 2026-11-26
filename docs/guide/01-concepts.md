# 01. Concepts

[Start here](00-start-here.md)

## Playback rig

Two computers play the same Ableton Live set into one iConnectivity PlayAUDIO1U. The Main Mini uses USB-C port A. The Backup Mini uses port B. The interface has 12 balanced XLR outputs. [PlayAUDIO1U guide](../manuals/playaudio1u-user-guide.pdf).

## Stems, click, and cues

A stem is a stereo (or mono) group of the song, not the whole mix. The suggested output map, which is not from a manual, is: 1 click, 2 guide/cues, 3–4 backing, 5–6 drums, 7–8 synth/bass, 9–10 FX, 11–12 spare. Click and cues go to IEM auxes only, not to the house mains. [Cable schedule](../cable-schedule.md).

## Redundancy and failover

Both Minis stay in time. If the Main USB cable drops, the PlayAUDIO1U switches to B without a gap in audio and MIDI, provided LifeSine is armed on output 15. A footswitch on a CONTROL port, or the touch panel, can switch by hand. [Cases](../cases-and-rack-layout.md).

## Sample rate, buffer, latency

The PlayAUDIO1U supports 44.1, 48, 88.2, and 96 kHz. The XR18 rate is not verified in this plan. Set them the same after reading the XR18 manual. **Unverified:** a required buffer size. Do not copy a number from another show.

Latency for MIDI over the network: stay wired. Apple’s current network-MIDI page does not publish a latency knob. [RTP-MIDI setup](../rtp-midi-setup.md).

## Clock and sync

In perform mode, Ableton Link is off and AbleNet keeps the two AbleSet computers together. In record mode, Link may be on, and RTP-MIDI can carry MIDI clock and transport. [Modes](../modes-and-checklists.md).

## MIDI, RTP-MIDI, AbleNet, OSC

- MIDI is the messages (notes, CC, clock).
- RTP-MIDI is MIDI inside network packets. Apple calls the setup a network MIDI session and offers an RTP session type. [Apple](https://support.apple.com/guide/audio-midi-setup/set-up-a-midi-network-session-ams1012/mac).
- AbleNet is AbleSet’s own link between computers. It is not RTP. [AbleNet](https://ableset.app/docs/ablenet).
- OSC is a different network message system. AbleSet Pro can send it on a timer with OSC Tracks. [OSC Tracks](https://ableset.app/docs/osc-tracks).

## DMX

DMX is the lighting control wire. This plan prefers a dedicated DMX cable from an Enttec USB interface on the Main Mini. Art-Net and sACN are network versions. Lightkey supports both USB-DMX and those protocols. [Lighting](../lighting-lightkey.md).

## HDMI and HDBaseT

Each M1 has one HDMI 2.0 output, up to 4K60, plus one Thunderbolt display. [Apple M1 specs](https://support.apple.com/en-us/111894). The KVM uses a Thunderbolt / USB 4 port. HDMI goes to a 2-in/1-out switch, then a 1x2 splitter, then HDBaseT for long Cat6A runs. HDBaseT is not Ethernet. Keep it off the data switch. [Video](../video-projectors.md).

## IEM mixes

The XR18 has six aux sends. Five mono mixes use Aux 1–5. Five stereo mixes do not fit. [IEM mixes](../iem-mixes.md).

## Gain staging

**Unverified:** target levels in dBu. The PlayAUDIO1U outputs are line level. The XR18 inputs receive them. Turn the house send down before the first playback. Click must not be in Main L/R.
