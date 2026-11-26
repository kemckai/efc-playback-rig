# Glossary

[Start here](00-start-here.md)

| Term | Meaning in this rig |
| --- | --- |
| Main Mini | Mac mini (M1, 2020), `192.168.1.11`. Live, AbleSet, Lightkey. PlayAUDIO1U DAW A. |
| Backup Mini | The other M1, `192.168.1.12`. Same perform set. PlayAUDIO1U DAW B. |
| Mini A / Mini B | Record-mode names for Main and Backup. |
| PlayAUDIO1U | iConnectivity interface. 12 XLR outs, two front USB-C DAW ports, LifeSine failover. |
| Auracle X | iConnectivity’s app that configures the PlayAUDIO1U. Not iConfig. |
| LifeSine | Free plugin. Tone on output 15 arms auto failover. |
| Scene A / B | Which Mini the PlayAUDIO1U is using. A is normal. |
| AbleNet | AbleSet’s link between the two computers. |
| RTP-MIDI | MIDI over the network. Apple Audio MIDI Setup, session type RTP. |
| OSC | A different network control protocol. AbleSet Pro OSC Tracks send it. |
| PERFORM | XR18 scene: aux 1–5 to IEMs, main to the snake. |
| REC-STUDIO | XR18 scene: USB 18x18 and studio monitors. |
| HDBaseT | Video over Cat6A. Not the data switch. |
| IEM | In-ear monitor. Five mono auxes. Model not confirmed. |
| Stem | A subgroup of the track, routed to its own XLR pair. |
| Bed | Channel-based part of an Atmos mix, up to 7.1.2 (ten channels). There is no 7.1.4 bed. [Atmos workflow](11-dolby-atmos-workflow.md). |
| Object | An Atmos channel with position metadata, not a fixed speaker. Up to 118 with one 7.1.2 bed. |
| ADM BWF | The usual Atmos music master: a Broadcast Wave file with Audio Definition Model metadata. |
| Dolby Audio Bridge | macOS driver that carries up to 128 channels from Live to the Renderer on one computer. |
| Music Panner | Dolby’s free plug-in that sends object positions from Live to the Renderer. |
| Re-render | A channel-based bounce from the Renderer (7.1.4, 5.1, binaural, stereo). |
| Binaural render mode | Off, Near, Mid, or Far on each bed or object, for Dolby headphone rendering. Not used by Apple Music Spatial Audio. [Atmos workflow](11-dolby-atmos-workflow.md#binaural-and-headphone-mixing). |
| Apple Spatial Audio | Apple’s own headphone (and some speaker) renderer for Atmos on Apple Music and Apple TV. It does not use Dolby binaural modes. |
| Trim and downmix | Metadata that controls how an Atmos mix folds to 7.1, 5.1, and stereo. |
| LFE | Low-frequency effects channel. An extension, not the only bass. |
