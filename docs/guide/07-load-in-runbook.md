# 07. Load-in runbook

[Eugene Fight Club playback rig](../../README.md)

The printable checkbox list is [SHOW-DAY-RUNBOOK.md](../../SHOW-DAY-RUNBOOK.md). Use that on the day. This chapter is the same order, in sentences, for reading before the gig.

The plan has no clock times. Work in this order: day before, placement, cabling, power-on, network, tablet, XR18 and IEMs, picture and lights, failover drill, pre-show, show, pack-out.

## Day before

Both Minis need the same Live set and the same samples. AbleSet warns that different sets change what happens when you jump songs. Pre-load the perform Audio MIDI Setup configuration so Mini-to-Mini RTP stays off. LifeSine on the Main set goes to output 15. The static-IP card must match the [network plan](../network-and-ip-plan.md).

Charge IEM and wireless batteries. The plan does not name the charger or the IEM model. The 1RU wireless item is still an assumption.

Pack three cases. Main: Furman, PlayAUDIO1U, switch, both Minis. Stage: XR18 and the IEM transmitters. Control: KVM, monitor, wired keyboard and mouse. The 4U main case has no front I/O panel, so the XLR loom leaves the rear.

## At the venue

Place the main case, the stage case, and the control case before you cable. Run the dual snake to FOH and confirm what it carries. Channel count and send/return are not confirmed.

Cable before power, in the order in the [cable schedule](../cable-schedule.md): PlayAUDIO1U USB-C A and B, KVM on the other Thunderbolt / USB 4 ports, HDMI into a 2-in/1-out switch (Main on 1, Backup on 2) then a 1x2 splitter and HDBaseT (never through the KVM), Ethernet to the switch, XLRs to the XR18, auxes to the IEMs, mains to the snake, footswitch to a CONTROL port, Enttec on a Main Mini USB-A.

## Power, then checks

The plan does not publish a power-on list. The runbook powers the Furman, then the switch, then the PlayAUDIO1U, then the Minis, then the XR18 (recall **PERFORM**), then the IEM transmitters, then the control case, projectors, and Lightkey. That order is so link lights, Scene A, and the show scene exist before you test them. Treat it as an operational sequence, not a manufacturer procedure.

Then walk the perform checklist in [Modes and checklists](../modes-and-checklists.md): static IPs, AbleNet on both, drift correction on the backup only, LifeSine shield icon, pull USB A, Sync Playback Now, five IEM mixes, Lightkey, and both projector inputs.

AbleNet and the tablet: open AbleSet from `192.168.1.11` or `192.168.1.12`. The plan does not name the web port; use the address in the AbleSet menu-bar window. Turn on Follow Current Audio Interface Scene on the tablet.

## Show and teardown

During the show, use the one-line table in the [show-day runbook](../../SHOW-DAY-RUNBOOK.md). Power-down is the reverse of power-on. The plan does not specify it.

## Unverified on purpose

- Clock times.
- Battery chemistry and charge time.
- How the set file is copied.
- AbleSet’s web port.
- Which XR18 channels are guitars or vocal mics.
- Which IEM product is in the case.
- Power-on and power-down as a manufacturer sequence.
