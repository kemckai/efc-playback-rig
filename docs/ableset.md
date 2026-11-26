# AbleSet on this rig

[Eugene Fight Club playback rig](../README.md)

Official docs home: [ableset.app/docs](https://ableset.app/docs). The same pages also answer on ableset.com. Prices in the parts list are AbleSet Standard $179 and Pro $269. Standard includes AbleNet and redundant-interface support. Pro adds the mixer, Canvas, and OSC Tracks. That split is the plan’s reading of the edition page; confirm it on [ableset.app](https://ableset.app/) before buying. **Unverified here:** a line-by-line feature matrix beyond the docs pages linked below.

The computers are two identical Mac mini (M1, Late 2020) units. Main is `192.168.1.11`. Backup is `192.168.1.12`. Mask `255.255.255.0`. [Network plan](network-and-ip-plan.md).

## Install on both Minis

**Unverified:** this guide did not find a click-path installer chapter that names a `.dmg` or a license-seat screen. The published introduction assumes the app is already installed.

What the introduction does say: AbleSet sits in the menu bar. Click it to open the main window. “Open AbleSet” opens a browser at the local address. The same address is shown in the menu-bar window for a phone or tablet on the same network. [Introduction](https://ableset.app/docs/introduction).

Install and authorize it on the Main Mini and the Backup Mini. Perform mode runs AbleSet on both, with the same Live set. [AbleNet](https://ableset.app/docs/ablenet).

## Song markers

AbleSet builds the setlist from Ableton locators. The simplest locator is the song title, placed at the start of the song. Put locators on a beat, preferably a downbeat. [Introduction](https://ableset.app/docs/introduction). [Locator notation](https://ableset.app/docs/locator-notation).

Notation the locator page documents:

- `> Verse 2` is a section. `>> Chorus` is a section pinned in performance view.
- Text in curly brackets is a description, for example `Follow Night {Tuning: C, Capo 1}`.
- `SONG END` is the end of the song. AbleSet then jumps to the next song if there is one.
- `STOP` or `AUTOSTOP` stops playback. A leading dot on the next song locator (`. Follow Night`) also stops at that boundary.
- `+LOOP` loops until the next locator. `+LOOPFULL` finishes the current loop before a jump. The plan’s video note uses `+LOOPFULL` for looping “video loop” songs. That flag is on this page.
- A leading `*` makes AbleSet ignore the locator.

Sections can also be MIDI clips on a Sections track from Live 11 onward. The setlist editor reorders songs. [Setlist editor](https://ableset.app/docs) is linked from the docs home. **Unverified:** the exact setlist-editor URL slug was not opened separately; the index lists “The Setlist Editor”.

## AbleNet: Main and Backup

1. Open the same Ableton session on both Minis.
2. Enable AbleNet in AbleSet’s settings on both. The computers connect and can be controlled together.
3. If Bonjour does not find the peer, Settings > AbleNet > Connect to Custom IPs. Main enters `192.168.1.12`. Backup enters `192.168.1.11`.
4. Drift correction uses Live’s Phase Nudge. Enable it on the backup only. Every audio clip must be warped. The page recommends Texture or Beats warp mode.
5. Sync Playback Now re-aligns the playhead after a crash. The page says this usually takes a few seconds.
6. Use Ethernet, not Wi-Fi, on stage.

[AbleNet](https://ableset.app/docs/ablenet).

Perform mode turns Link off, because AbleNet handles sync. Record mode turns AbleNet off. [Modes](modes-and-checklists.md).

## Wired tablet

Tablets use the owned Ethernet adapters and `192.168.1.51` through `.55`. [Network plan](network-and-ip-plan.md).

AbleSet’s switch section says a switch often does not hand out addresses. Set Configure IPv4 to Manually, keep the first three octets the same, and set the mask to `255.255.255.0`. [Connecting from other devices](https://ableset.app/docs/network).

On the tablet, open the address shown in the Mini’s AbleSet menu-bar window. You can start from either `192.168.1.11` or `192.168.1.12`. If that computer drops, AbleSet redirects to the next one. [AbleNet](https://ableset.app/docs/ablenet).

**Unverified:** the TCP port of the web UI. Do not guess it. Read it from the menu-bar window.

Turn on Follow Current Audio Interface Scene on the tablet so the browser follows the Mini that is actually selected on the PlayAUDIO1U. You can leave that option off on the Minis themselves. [Redundant audio interfaces](https://ableset.app/docs/audio-interfaces).

## Video in Ableton

AbleSet does not play video by itself. The plan’s video page, and AbleSet’s OSC Tracks page, are the sources.

- Live’s video window is one picture, Arrangement View, QuickTime `.mov`. It hides when Live’s main window loses focus. That limit is from Ableton and from an AbleSet forum thread, summarized in [Video](video-projectors.md).
- OSC Tracks are Pro. Name a MIDI track so it contains `+OSC`. Clips on that track send the OSC command in the clip name when the playhead reaches them. A command can target another app with `ip:port/address`. [OSC Tracks](https://ableset.app/docs/osc-tracks).
- The plan’s documented video route is OSC Tracks to a player such as QLab (`port 53000`, `/cue/{n}/start`), or a MIDI track into QLab, or `+LOOPFULL` on looping “video loop” songs. **Unverified in this pass:** the QLab port was in the rig plan’s video notes and was not re-checked against a QLab manual.
- This M1 has one HDMI 2.0 output for projectors. Both Minis meet at a 2-in/1-out HDMI switch, then a 1x2 splitter. [Video](video-projectors.md).

## MIDI and OSC

MIDI mapping: Settings > Edit MIDI Mapping, under “MIDI Mapping, OSC & Scripting”. Add a mapping and send the control. Notes, PC, and CC can be mapped. The Go button is play, next song, or loop escape depending on state. [MIDI mapping](https://ableset.app/docs/midi-mapping).

The AbleNet toggle on each MIDI input stays off in this perform rig, because both Minis already receive MIDI through the PlayAUDIO1U. Turn it on only if a single computer receives the controller. [MIDI mapping](https://ableset.app/docs/midi-mapping).

OSC control is a Pro page: [Controlling AbleSet via OSC](https://ableset.app/docs/osc). OSC Tracks can also target lighting desks and video players. [OSC connections](https://ableset.app/docs) is listed from the docs home. **Unverified:** the older plan said AbleSet listens on port 39051. That number was not re-read on the OSC page in this pass. Confirm it on [the OSC page](https://ableset.app/docs/osc) before you hard-code a port.

## Failover with the PlayAUDIO1U

AbleSet detects PlayAUDIO12, PlayAUDIO1U, and PlayAUDIO2U over USB. [Redundant audio interfaces](https://ableset.app/docs/audio-interfaces).

1. Cable Main to USB-C DAW A and Backup to USB-C DAW B. Scene A starts active. [Cases](cases-and-rack-layout.md).
2. Assign each computer to an interface scene in AbleSet if you want the browser to show which machine is live.
3. Enable Follow Current Audio Interface Scene on the tablet.
4. `+FOLLOWSCENE` (or `+FS`) on a track name unmutes that track only on the computer the interface has selected.
5. Arm LifeSine on output 15 on the Main Mini. Pull the DAW A USB cable in soundcheck. Audio should continue on B. Then Sync Playback Now. [AbleNet](https://ableset.app/docs/ablenet).
6. iConnectivity communicates with AbleSet over the USB MIDI connection automatically. If you ever attach two iConnectivity interfaces, give them different names in Auracle and reconnect them. [Redundant audio interfaces](https://ableset.app/docs/audio-interfaces).

Auracle X, not a separate iConfig step, is the PlayAUDIO1U configuration app. [Auracle X](https://www.iconnectivity.com/auracle-x-series).
