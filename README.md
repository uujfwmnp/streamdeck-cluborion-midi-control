# Club Orion Reactive Lighting MIDI Control
This Stream Deck profile allows you to control the reactive lighting system inside VR Chat's "Club Orion" via MIDI. The following controls are mapped:
* Lighting animations 1-8
* All colors, including split colors and their related color cycle buttons
* All flasher/strobe settings
* Almost all EQ settings *(band sliders and band gain coming soon)*
* Blinder strobe
* Disco ball
* Blackout toggle
* Fog Machine!

There are plenty of blank spots in most pages, if you want to add your own custom MIDI mapping or whatever else you need.

## Requirements:
* Stream Deck, Stream Deck Mk.2, or Stream Deck XL (profile will not work on SD Mini or SD Mobile)
* Stream Deck MIDI plugin
* LoopMIDI program - https://www.tobias-erichsen.de/software/loopmidi.html

## Installation
1. Install the Stream Deck MIDI plugin from the Stream Deck program itself
2. Install the LoopMIDI program, and create a new port called `StreamDeck2DawTrack`
3. Add the following to the VR Chat launch options: --midi=StreamDeck2DawTrack
4. Import the `Club Orion Lighting System.streamDeckProfile` file

## Using MIDI Controls
1. Make sure LoopMIDI is running & your Stream Deck is running the lighting profile
2. Run VR Chat and load into a Club Orion instance
3. Set yourself as an approved DJ/mod, then toggle the Audio Reactive Controls button
4. Click/tap the "Enable MIDI" button to open the MIDI recording/mapping screen
5. Copy and paste the following string into the "IMPORT STRING" field:
```
*|^0, &60$|^1, &60$|^2, &60$|^3, &60$|^4, &60$|^5, &60$|^6, &60$|^7, &60$|^12, &60$|^14, &60$|^0, &1$|^1, &1$|^2, &1$|^3, &1$|^4, &1$|^5, &1$|^6, &1$|^7, &1$|^8, &1$|^9, &1$|^10, &1$|^11, &1$|^0, &0$|^1, &0$|^3, &0$|^2, &0$|^4, &0$|^15, &60$|^13, &60$|^0, &2$|^1, &2$|^2, &2$|^3, &2$|^4, &2$|^5, &2$|^6, &2$|^7, &2$|^8, &2$|^9, &2$|^10, &2$|^11, &2$|%EXDEE%EXDEE%^0, &0$%^1, &0$%^2, &0$%^3, &0$%EXDEE%EXDEE%EXDEE%EXDEE%EXDEE%EXDEE%EXDEE%EXDEE%EXDEE%^4, &0$%EXDEE%EXDEE%EXDEE%EXDEE%^5, &0$%^6, &0$%^7, &0$%^8, &0$%*
```
6. Click/tap the "Import (from String)" button. You should see green text appear to tell you it has been successfully imported
7. Press any button on your Stream Deck, and you should see the change correspond in game.
8. For changing EQ settings, press and hold to change in one direction. Double tap and hold to change in the opposite direction.
9. *(Optional)* "Sync" the page 2 EQ sliders/knobs by holding each button to move the slider to full min or max, then back to in-game default center, then click/tap the "Reset" button.

**Note: VR Chat does not currently send MIDI data back out, so the deck meter icons will only be a rough estimate of where each EQ level is set.**

## Troubleshooting
* Make sure LoopMIDI is running before you launch VR Chat.
* Make sure you have created the `StreamDeck2DawTrack` port in LoopMIDI.
* Make sure you have added `--midi=StreamDeck2DawTrack` to the VR Chat launch options, and ensure the spelling is correct.
