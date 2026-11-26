# 04. XR18 and IEM mixing

[Start here](00-start-here.md)

The XR18 is the on-stage mixer: PlayAUDIO1U returns in, Aux 1–5 to five mono IEM mixes, Main L/R to the dual snake. That role is still an assumption until FOH confirms the snake. [IEM mixes](../iem-mixes.md).

## What the manual establishes

The X AIR manual covers the XR18’s USB 18x18 audio and MIDI, the REMOTE switch (Ethernet, Wi-Fi client, or its own access point), and X AIR EDIT for Mac from behringer.com. [XR18 product page](https://www.behringer.com/en/products/0605-AAD). [English manual](https://mediadl.musictribe.com/media/PLM/data/docs/X-AIR/M_BE_0605-AAA_X-AIR_EN.pdf).

This show sets REMOTE to Ethernet and the mixer to `192.168.1.20`. Do not leave it on `192.168.1.1`, which is the address it uses as a DHCP server. [Network plan](../network-and-ip-plan.md).

The manual’s first-connection steps use Access Point mode and then X AIR EDIT’s Setup list. That is the factory Wi-Fi path, not this show’s Ethernet path. **Unverified:** the exact Ethernet static-IP clicks inside X AIR EDIT. Set the address, then confirm the app sees `192.168.1.20`.

## Scenes

Save **PERFORM**: aux 1–5 to IEMs, main to the snake, USB not required. Save **REC-STUDIO**: USB routing and studio monitors. [Modes](../modes-and-checklists.md).

**Unverified:** the snapshot button names in the current X AIR EDIT build. The plan calls them scenes PERFORM and REC-STUDIO. Store those two and recall them from the show-day list.

## Five mixes

Aux 1 through 5, one mono mix per player. Aux 6 spare. Stereo would use two auxes each, so three stereo mixes is the maximum. [IEM mixes](../iem-mixes.md).

Players can open the X AIR app on a wired tablet and edit their own aux. That depends on the switch staying up. Wired P16-M mixers are the other option in the plan. They use Ultranet and wired earbuds, not the wireless IEMs.

## Guitars and mics

The suggested playback map leaves four XR18 mic/line inputs if all 12 PlayAUDIO1U outputs are patched. The plan does not assign SM58, SM57, Beta 52A, e906, M5, AT2020, or a guitar wireless system to those inputs. Shure GLXD16+ and Line 6 Relay G10SII are under consideration only. See the [manuals index](../manuals/README.md).

Scan wireless at the venue. Stay out of 617–652 MHz and 663–698 MHz. [IEM mixes](../iem-mixes.md).
