# SCFW-Emus4Clones
A collection of modified binaries guaranteed to consistently work on clone GBAs like the Digi Retroboy, EXEQ GameBox SP, K1 GBA SP, etc...
This is primarily intended to be used on a SuperCard SD with SCFW, but it should also be usable on existing ROM builders.

# Emulator table
Modified emulator binary | Basis / source | How to
:-:|:-:|:-:
cologneV0.8-splashed.gba | [Cologne V0.8](https://www.zophar.net/consoles/gameboy/coleco/cologne.html) | Rename this to `cologne.gba`
jagoombacolorV0.5-splashed.gba | [Jagoomba Color V0.5](https://github.com/EvilJagaGenius/jagoombacolor)  | Rename this to `gb.gba` & make a copy named `gbc.gba`
NGPGBA-DoubleROM-nosplash-base.gba |  [NGPGBA V0.5.7](https://github.com/FluBBaOfWard/NGPGBA) | Rename this to `ngp.gba`
pceadvanceV7.6-DoubleROM-splashed-base.gba | [PCEAdvance V7.5](https://www.zophar.net/consoles/gameboy/tg16/pceadvance.html) | Rename this to `pcea.gba`
pocketnesV9.98-maxzhou88-splashed.gba | [Maxzhou88 PocketNES V9.98](http://maxzhou88.ysepan.com/) | Rename this to `nes.gba`
SMSAdvanceV2.5-splashed.gba | [SMSAdvance V2.5](https://web.archive.org/web/20150430211123/http://www.ndsretro.com/gbadown.html) | Rename this to `smsa.gba`
SwanGBA_V0.6.7-splashed.gba | [SCFW SwanGBA V0.6.7](https://github.com/OmDRetro/SwanGBA-SCFW) | Rename this to `bwsc.gba`

# Modified build description
Modified emulator(s) | Description
:-:|:-:
Cologne, Jagoomba Color, SMSAdvance, SwanGBA | These emulators do not consistently run on a GBA clone with a SuperCard SD running SCFW. In order to add some consistency, I added in a splash screen.
NGPGBA | This emulator, version 0.5.7, does NOT support splash screens. In order to make this consistently run on a GBA clone, I had to add in a [free redistributable homebrew](https://pdroms.de/files/snk-neogeopocket-ngp-neogeopocketcolor-ngpc/3d-techdemo-v1-0) made by [@THOR](https://thor.pdroms.de/) who's known in some online Neo Geo Pocket Homebrew community. This will force the user to select the ROM they intend to run via menu by holding `L` and `R`, but it definitely is better than not being able to run the emulator on a GBA clone.
PCEAdvance | This emulator is a tricky one. Not only did I have to add a splash screen, but I had to add in a "dummy" ROM. I currently do not have the knowledge to make one so instead I used a copy of the [240p test suite](https://github.com/ArtemioUrbina/240pTestSuite) by Artemio Urbina. Much like NGPGBA, the user will be forced to select their intended ROM by holding `L` and `R` then load the ROM manually.
PocketNES V9.98 by Maxzhou88 | [Maxzhou88](https://hiddenpalace.org/Maxzhou88) the person who created the K1 GBA, REVO K101, etc... actually created a custom build of the famous PocketNES emulator. Since EWRAM overclock does NOT work on clones, this build adds an automated speedhack feature in its place. Works well on both authentic GBAs as well as clones!
