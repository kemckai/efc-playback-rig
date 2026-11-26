# FAQ

[Start here](00-start-here.md)

## Which Mac is this?

M1 confirmed. Two identical Mac mini (M1, Late 2020) units, 16GB unified memory, 512GB SSD. [Apple](https://support.apple.com/en-us/111894). The renewed pair in the parts list is $605 each, $1,210, Amazon Renewed Excellent, Techdeals4Less, 26 November 2026.

## Does the 1U Sonnet mount fit?

Yes. Sonnet’s note says RACK-MIN-2XA is fully compatible with M1 Mac minis. The chassis is 1.4 in tall. The case stays the Gator GR-4S. [Cases](../cases-and-rack-layout.md).

## Why not five stereo IEM mixes?

The XR18 has six auxes. Stereo needs two each, so three stereo mixes is the maximum. This plan is five mono mixes. [IEM mixes](../iem-mixes.md).

## Do I leave RTP connected at a show?

No. Perform mode turns Mini-to-Mini RTP off or unrouted so transport is not doubled. Record mode turns it on. [RTP-MIDI setup](../rtp-midi-setup.md).

## Who configures the PlayAUDIO1U?

Auracle X, from iConnectivity. [Auracle X](https://www.iconnectivity.com/auracle-x-series). An iConfig manual for this unit was not found.

## Can both projectors show the Backup?

Yes, if you select input 2 on the 2-in/1-out HDMI switch. The 1x2 splitter then feeds both screens. A 2x2 matrix is the unpriced alternative. [Video](../video-projectors.md).

## Where is the printable list?

[SHOW-DAY-RUNBOOK.md](../../SHOW-DAY-RUNBOOK.md).

## Does the Renderer change my 7.1.4 mix?

It can. Live’s 7.1.4 mix is twelve channels, not an Atmos master. Map the four heights as objects (or pin objects to those speakers), then record and export from the Renderer or from Fiedler Composer. [Atmos workflow](11-dolby-atmos-workflow.md).

## Why does 5.1 lose my height placements?

5.1 has no height speakers, so overhead energy folds into the floor. Direct Render and manual trims change the balance, but they cannot keep elevation. [Folding down to 5.1](11-dolby-atmos-workflow.md#folding-down-to-51-loses-my-placements).

## Do I have to use the Dolby Atmos Renderer app?

No. You need a Dolby-approved renderer to write an ADM BWF. That can be the Renderer app with the Music Panner, or Fiedler’s Dolby Atmos Composer inside Live. A 12-channel 7.1.4 WAV is not Atmos. [Do I have to use the Renderer?](11-dolby-atmos-workflow.md#do-i-have-to-use-the-dolby-atmos-renderer).

## Why does the Music Panner sequencer only do mono?

Atmos objects are mono. A stereo sound is two objects, linked with Copy or Mirror. The sequencer typically drives one path; the second object follows the link. Split to two mono tracks if left and right must move on their own. [Sequencer FAQ](11-dolby-atmos-workflow.md#why-does-the-panner-sequencer-only-do-mono).

## Does Apple Music use my binaural render modes?

No. Apple Music headphone playback uses Apple’s Spatial Audio renderer and ignores Off, Near, Mid, and Far. Check that path separately. [Binaural and headphone mixing](11-dolby-atmos-workflow.md#binaural-and-headphone-mixing).
