# Show-day runbook

Print this. Check the boxes. Deeper notes are linked; this page is the order of work.

This is the **perform** (redundant playback) day. Record / studio settings are in [Modes and checklists](docs/modes-and-checklists.md). The plan does not give clock times. Sections are in order. Anything the plan does not specify is marked **Unverified**.

Cases: [main 4U](docs/cases-and-rack-layout.md) (Furman, PlayAUDIO1U, switch, both Minis), [stage](docs/iem-mixes.md) (XR18 and IEM transmitters), [control](docs/cases-and-rack-layout.md) (KVM, 15.6 in monitor, wired keyboard and mouse).

## 1. The day before

- [ ] Charge IEM receiver batteries and any wireless transmitter batteries. **Unverified:** the plan does not name a charger or a charge time. The 1RU wireless item is still assumed to be IEM transmitters and is not confirmed.
- [ ] Put the same Live set and the same samples on Main and Backup. AbleSet warns that a different set on each computer changes behaviour when jumping songs. **Unverified:** the copy method (drive, network, or otherwise) is not specified.
- [ ] Confirm both Minis are the same sample rate. The PlayAUDIO1U supports 44.1, 48, 88.2, and 96 kHz. The XR18 rate is not verified; set both to the same rate after checking the XR18 manual.
- [ ] On both Minis, pre-load the perform Audio MIDI Setup configuration (Mini-to-Mini RTP sessions off or unrouted).
- [ ] Confirm LifeSine is on the Main set, routed to output 15.
- [ ] Confirm the laminated static-IP card matches [the IP plan](docs/network-and-ip-plan.md): Main `192.168.1.11`, Backup `192.168.1.12`, PlayAUDIO1U `192.168.1.13`, XR18 `192.168.1.20`, tablets `192.168.1.51`–`.55`, mask `255.255.255.0`. Main has no gateway. Do not use `192.168.1.1` on the XR18.

**Pack — main case:** Furman M-8x2, PlayAUDIO1U, TL-SG1016D, Sonnet mount with both Minis, IEC cord, labeled rear XLR loom. The 4U case has no front I/O panel.

**Pack — stage case:** XR18, its power supply, five IEM transmitters (or the unconfirmed 1RU wireless units), XLR for Aux 1–5 and Main L/R.

**Pack — control case:** USB-C KVM, ASUS ZenScreen, wired keyboard and mouse, one USB-C cable per Mini, extension lead for the Furman.

**Pack — loose:** dual snake (channel count and send/return not confirmed), footswitch and 1/4 in TRS, wired tablets and owned Ethernet adapters, DMX interface and dedicated DMX cable, two projectors, 2x1 HDBaseT switchers, 1x2 HDMI splitters, Cat6A for video (not through the data switch), Cat5e or Cat6 for the data switch.

- [ ] Cases closed and labeled. Cables labeled.

## 2. Load-in and placement

- [ ] Main case where the operator can reach the KVM cables and the rear XLRs.
- [ ] Stage case at the stage box: XR18, IEM transmitters on or beside it.
- [ ] Control case at the operator: monitor, KVM, keyboard, mouse.
- [ ] Projectors and HDBaseT receivers at the screens. Keep HDBaseT off the data switch. Extenders are not Ethernet.
- [ ] Dual snake run to FOH. Confirm with FOH what it carries before patching mains.

## 3. Cabling order

Do this before power. Map: [cable schedule](docs/cable-schedule.md).

- [ ] Main Mini Thunderbolt to PlayAUDIO1U front USB-C A (audio and MIDI).
- [ ] Backup Mini Thunderbolt to PlayAUDIO1U front USB-C B.
- [ ] Other Thunderbolt on each Mini to the USB-C KVM (video, keyboard, mouse). Not the projector path.
- [ ] Main HDMI to input 1 of a 2-in/1-out HDMI switch. Backup HDMI to input 2. Switch output into a 1x2 splitter, then HDBaseT toward the projectors. Never through the KVM. A 2x2 matrix is the alternative if each projector is selected on its own. No model or price is in the plan.
- [ ] Each Mini Ethernet and the XR18 Ethernet to the gigabit switch. XR18 REMOTE set to Ethernet.
- [ ] Tablets to the switch with the owned Ethernet adapters.
- [ ] PlayAUDIO1U XLR 1–12 to the XR18. Leave output 15 unpatched (LifeSine is internal).
- [ ] XR18 Aux 1–5 to the five IEM transmitter inputs. Main L/R to the snake.
- [ ] Footswitch 1/4 in TRS to a PlayAUDIO1U CONTROL port.
- [ ] Lightkey: Enttec on a Main Mini USB-A, then dedicated DMX to the fixtures. Do not use the PlayAUDIO1U front USB-A host port (it is broken).
- [ ] One extension lead from the Furman to a small strip in the control case.

Suggested playback map (a starting suggestion, not from a manual): 1 click (aux only, not main), 2 guide/cues (aux only), 3–4 backing, 5–6 drums, 7–8 synth/bass, 9–10 FX, 11–12 spare.

## 4. Power-on order

The plan does not publish a power-on sequence. This order exists so each later check has power. **Unverified** as a manufacturer procedure.

1. [ ] Furman M-8x2 first. It feeds the case, and the control-case strip hangs off it.
2. [ ] Gigabit switch. Later checks need link lights. There is no DHCP and no router.
3. [ ] PlayAUDIO1U. Scene A should be the active scene before the Minis stream.
4. [ ] Both Minis. Each one needs the PlayAUDIO1U and the KVM already cabled.
5. [ ] XR18, then recall scene **PERFORM** (aux 1–5 to IEMs, main to the snake).
6. [ ] IEM transmitters after PERFORM is up, so they send the show auxes.
7. [ ] Control-case monitor and KVM.
8. [ ] Projectors and HDBaseT switchers.
9. [ ] Enttec / Lightkey path on the Main Mini.

## 5. Network, RTP-MIDI, and AbleNet

Addresses: [network plan](docs/network-and-ip-plan.md). Sessions: [RTP-MIDI setup](docs/rtp-midi-setup.md).

- [ ] Switch link lights on for both Minis, the XR18, and the tablets.
- [ ] Main `192.168.1.11`, Backup `192.168.1.12`, mask `255.255.255.0`. Main: no gateway.
- [ ] PlayAUDIO1U `192.168.1.13` if it is set static in Auracle X.
- [ ] XR18 `192.168.1.20`, not `192.168.1.1`.
- [ ] Perform Audio MIDI Setup: Mini-to-Mini RTP sessions off or unrouted. Both Minis already get the same MIDI through the PlayAUDIO1U. Leaving RTP up can duplicate transport.
- [ ] Wi-Fi off for the show network. Latency note in the plan: wired only, no Wi-Fi, unmanaged switch, short Cat6.
- [ ] Same Live set and AbleSet open on both Minis. AbleNet on both.
- [ ] If Bonjour does not see the peer, enter the other Mini’s IP under Connect to Custom IPs.
- [ ] Drift correction (Phase Nudge) on the backup only. All audio clips warped.
- [ ] AbleSet MIDI AbleNet toggle off. Both computers receive MIDI.
- [ ] Link off. AbleNet handles perform sync.

## 6. Tablet

- [ ] Tablet on a wired Ethernet adapter, address in `192.168.1.51`–`.55`.
- [ ] Browser opens AbleSet at a Mini’s address (`.11` or `.12`). The plan does not name the web port. Use the address shown in that Mini’s AbleSet menu-bar window. **Unverified:** the port number.
- [ ] Follow Current Audio Interface Scene on, so the tablet follows whichever Mini is sending audio.
- [ ] X AIR app opens the XR18 at `192.168.1.20` if players will mix their own aux. That depends on this network staying up.

## 7. XR18, line check, IEMs, RF

Scene **PERFORM**. Five mono mixes use Aux 1–5. Aux 6 stays spare. One mono mix per player. Stereo mixes do not fit five players.

- [ ] Click on output 1 is in the auxes only, not in Main L/R.
- [ ] Guide/cues on output 2 are aux only.
- [ ] Line-check each patched PlayAUDIO1U return into the XR18 (outs 1–12).
- [ ] Line-check any live inputs on the XR18. The suggested map leaves four mic/line inputs if all 12 playback outs are patched. **Unverified:** which live sources those four are. Guitar wireless and vocal mics are not assigned to channels in this plan.
- [ ] IEM 1 through 5: each player hears only their aux, plus click if that aux includes it.
- [ ] PlayAUDIO1U headphone jack can be a click-only backup for one player (two independent headphone mixes).
- [ ] Scan at the venue with the transmitter maker’s frequency tool. Five channels need coordinated frequencies.
- [ ] Stay out of 617–652 MHz and 663–698 MHz. Avoid Sennheiser XSW band C (662–686 MHz). **Unverified:** which IEM model is in the case, so the scan tool depends on that choice.

## 8. Projectors and Lightkey

- [ ] HDMI switch on input 1 (Main): both projectors show that picture after the 1x2 splitter.
- [ ] HDMI switch on input 2 (Backup): both projectors show the Backup.
- [ ] Projector path is HDMI, not the KVM.
- [ ] A crashed app on a live Mac can still output a picture, so an auto HDMI switch may not trip. Use the manual select.
- [ ] Lightkey is running on the Main Mini. Enttec output and the DMX run look right.
- [ ] One Lightkey license is active on one Mac. Do not plan to move the license during a song. On a Main failure, a USB interface with its own microprocessor holds the last look. Some cheap interfaces send zeros and can flicker.

## 9. Failover drill

From the perform checklist and the PlayAUDIO1U steps.

- [ ] Shield icon on the PlayAUDIO1U is blinking (LifeSine armed on output 15).
- [ ] Playback is running on both Minis.
- [ ] KVM is on the Backup for this test, to see that it is tracking.
- [ ] Pull the USB cable from PlayAUDIO1U DAW A. Audio and MIDI should continue on B.
- [ ] Sync Playback Now in AbleSet.
- [ ] Select HDMI switch input 2 and confirm both projectors follow the Backup. Select input 1 again.
- [ ] Put the USB cable back on DAW A and confirm Scene A is active again before doors.
- [ ] Footswitch on the CONTROL port does a manual failover (assigned in Auracle X). Touch panel can also switch.

## 10. Pre-show final

- [ ] Scene A active, LifeSine armed, footswitch assigned.
- [ ] XR18 on PERFORM. USB from the XR18 is not plugged into a Mini.
- [ ] Five IEM mixes and click verified.
- [ ] FOH has Main L/R from the snake.
- [ ] Lightkey and both projector inputs checked.
- [ ] Tablet shows the computer that is sending audio.
- [ ] First song: leave the KVM on the Backup long enough to see that it tracks the Main.

## 11. During the show

One line each. Then use the linked page if it is still wrong.

| What you see | Do this |
| --- | --- |
| No playback audio | Confirm Scene A, both USB-C DAW cables, and the blinking shield. Then XR18 PERFORM and Main L/R to the snake. [Modes](docs/modes-and-checklists.md) |
| Failover already happened | Leave B playing. Sync Playback Now. Do not move the Lightkey license mid-song. Switch projectors by hand if the picture did not follow. [Video](docs/video-projectors.md) |
| Clicks or double transports | Mini-to-Mini RTP should be off. AbleSet MIDI AbleNet toggle should be off. [RTP-MIDI](docs/rtp-midi-setup.md) |
| Tablet blank | Open the other Mini’s address (`.11` or `.12`). Check the Ethernet adapter and link light. [Network](docs/network-and-ip-plan.md) |
| Projector dark | Select the other input on the 2-in/1-out HDMI switch. Check the 1x2 splitter. Do not send projectors through the KVM. |
| One IEM drops | That player can use the PlayAUDIO1U headphone click backup. Rescan only between songs. [IEMs](docs/iem-mixes.md) |
| Click in the house | Output 1 must stay out of Main L/R. Auxes only. |
| Lights stuck | Expected if the Main Mini stopped and the Enttec holds the last look. Second license is the only fast lighting backup, and only if you already own it. [Lightkey](docs/lighting-lightkey.md) |

## 12. Power-down and pack-out

The plan does not specify power-down. This is the reverse of section 4 so a device is not still streaming into a box you are unplugging. **Unverified** as a manufacturer procedure.

- [ ] Stop playback on both Minis.
- [ ] IEM transmitters off.
- [ ] Projectors and HDBaseT off.
- [ ] Lightkey quit. Enttec unplugged.
- [ ] XR18 off.
- [ ] Minis shut down.
- [ ] PlayAUDIO1U off.
- [ ] Switch off.
- [ ] Furman off last.
- [ ] Pack the three lists in section 1. Label anything that was re-patched.
- [ ] Note which IEM frequencies were clean, and whether the dual snake was send-only or send and return.

## Where to read next

- [Perform and record checklists](docs/modes-and-checklists.md)
- [Cable schedule](docs/cable-schedule.md)
- [Cases and rack layout](docs/cases-and-rack-layout.md)
- [IEM mixes](docs/iem-mixes.md)
- [Load-in chapter](docs/guide/07-load-in-runbook.md)
