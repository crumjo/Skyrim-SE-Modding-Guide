# Skyrim SE Modding Guide #



---------------
## Objective ##
This project seeks to provide a walkthrough to modding Skyrim SE from start to
finish. This walkthrough is intended to be for anyone, regardless of their
modding experience. I wrote this while going through the process of modding a
fresh Skyrim SE install using Mod Organizer 2 (MO2). While there are other
managers out there, such as Vortex or Nexus Mod Manager (NMM), I have found MO2
to be my favorite.

This project is a walkthrough, and not intended to be used as a comprehensive
guide for any of the tools used. All tools are well documented so please refer
to their Nexus page for more information.


-----------------
## Preparation ##

### Nexus Mods ###

- Create a [NexusMods](https://www.nexusmods.com/skyrimspecialedition) account.
  This is where almost all of the mods used in this walkthrough can be
  downloaded from.


### Clean Skyrim SE Installation ###

- Avoid installation on _C:\\_ drive if possible. If _C:\\_ is the only
  option, install anywhere except _Program Files_ or _Program Files (x86)_.

- Disable Steam automatic updates and the Steam overlay.

- Start game and select ultra preset if auto-detect fails and then load into
  the main menu. This is done in order to generate _.ini_ settings files.


### 7-Zip (Optional) ###
[7-Zip](https://www.7-zip.org/) is a free and open source file archive tool
  that I would highly recommend.
  MO2 works natively with .7z archive files, but standard zip files work too.

### Folder Setup (Optional) ###
This is an optional step, but I like to configure a sensible folder structure
to make life and mod managing easier.

- I have a separate SSD with a folder called "Mods". Inside this folder, I have
  created several subfolders:

  a. _Mod Organizer 2 Mods_ - Location for installed and downloaded mods. Mod
     Organizer 2 will create several subfolders here after completion of the
     next step.

  b. _Manual Mods_ - Location for mods not downloaded through MO2.

  c. _Tools_ - Installation location for all tools used in this walkthrough.

  d. _Skyrim Special Edition - Shortcut_ - Shortcut to the base Skyrim
     installation Steam folder for quick access.


### Mod Manager Installation ###

- [Mod Organizer 2](https://www.nexusmods.com/skyrimspecialedition/mods/6194)
  is my personal favorite, download and run the installer from Nexus.

- The installer should create a start menu shortcut. Right click this shortcut
  and follow _More > Open file location > Shortcut > Advanced..._ and check
  the _Run as administrator_ checkbox. Now MO2 will always run with
  administrator privileges when you use the start menu to launch it, which
  reduces potential file permission issues.

- Create a folder anywhere you want to store your mods (even on a different
  drive). Keep in mind that this folder can grow to be quite large depending on
  how many mods you have, so plan accordingly. If you decided to follow my
  folder configuration from the previous step, point MO2 to
   _Mod Organizer 2 Mods_

- Run MO2 and point it to the mod folder you just created:
  _Tools > Settings... > Paths > Base Directory_


### LOOT Installation ###
LOOT (Load Order Optimization Tool) is a program that we will use to set a load
order for the installed mods in our game. This is important for stability.

- Download [LOOT](https://www.nexusmods.com/skyrimspecialedition/mods/1918)
  from Nexus and run the installer.

- Add LOOT executable to MO2 so that it can be launched from there:
  _Tools > Executables > + > Add from file... > locate your LOOT executable_

- Run LOOT from MO2, it should auto detect your game and flag _Update.esm_,
  _Dawnguard.esm_, _HearthFires.esm_, and _Dragonborn.esm_ as dirty plugins.

- Close LOOT, we will come back to it later.


### Clean Master Files ###
SSEEdit is a an "advanced graphical module viewer/editor and conflict detector"
that we will use to clean the 4 master files to improve stability. **Do not
clean any dirty plugins downloaded from Nexus unless the installation
instructions tell you to.**

1. Download and extract
   [SSEEdit](https://www.nexusmods.com/skyrimspecialedition/mods/164) using
   7-Zip.

2. Add _SSEEditQuickAutoClean.exe_ executable to MO2.

3. Run _SSEEditQuickAutoClean.exe_ on each plugin _individually_ in the
   order below, closing SSEEdit between cleanings. The message "Background
   Loader: finished" should appear the plugin cleaning is complete.

   a. _Update.esm_

   b. _Dawnguard.esm_

   c. _HearthFires.esm_

   d. _Dragonborn.esm_

4. Create a new archive with the cleaned plugins so that updates to do not
   revert them back to their old dirty state. The location of the plugins is:
   _[Skyrim Base Folder]/Data_. Ctrl click _Update.esm_, _Dawnguard.esm_,
   _HearthFires.esm_, _Dragonborn.esm_ and then right click to bring up the
   context menu, and then: _7-Zip > Add to data.7z_

5. Install the cleaned masters via MO2:
   _Install a new mod from an archive (top left) > locate data.7z > manual >
   check all boxes > ok_

6. After activating the mod (checking the box in the left pane), you should see
   white lightning bolts next to the 3 DLCs, indicating that they have been
   completely overwritten.

7. Either delete _data.7z_ from the Skyrim Data folder or move it somewhere
   else (I rename and keep mine in the "Other Mods" folder).



-----------------------
## SKSE Installation ##

1. Download and extract the latest SE build for the
   [Skyrim Script Extender](https://skse.silverlock.org/).

2. Copy both _.dll_ files and _skse64_loader.exe_ to Skyrim's base installation
   folder.

3. Create a shortcut in MO2 to _skse64_loader.exe_ and launch the game
   with this from now on. This is required for SKSE to work properly.

4. Send the _Scripts_ folder, located inside of the _Data_ folder of SKSE, to a
   7-Zip or standard zip archive and install manually via MO2.



---------------
## Core Mods ##

See 'core' in mods directory.



---------
## ENB ##

1. Download and extract the enb binaries from
   [enbdev](http://enbdev.com/download_mod_tesskyrimse.htm)

2. Copy and paste _enbseries_, _d3d11.dll_, and _d3dcompiler_46e.dll_ to
   Skyrim's base folder from _Wrapper Version_.

3. Download and extract the enb of your choice from Nexus and follow the
   author's installation instructions. Most enbs can be installed by simply
   copying _enbseries_, _enblocal.ini_, & _enbseries.ini_ to Skyrim's base
   folder, but some will have other dependencies (patches, weather mods, etc.)


### Additional ENB Mods ###

See 'enb_lighting' in mods directory.



-------------
## BethINI ##

- Download and extract
  [BethINI](https://www.nexusmods.com/skyrimspecialedition/mods/4875).

- **Do not** add shortcut to MO2. BethINI and MO2 cannot run at the same time.

- Close MO2 and run BethINI.

- Make the tweaks recommended by your chosen ENB's README file.



-----------------
## My Mod List ##


### Large Texture Packs ###

See 'large_texture_packs' in mods directory.


### Weather & Atmosphere ###

See 'weather_atmosphere' in mods directory.


### Landscape ###

See 'landscapes' in mods directory.


### Clutter ###

See 'clutter' in mods directory.


### Vegetation ###

See 'vegetation' in mods directory.


### Cities ###

See 'cities' in mods directory.


### Mines, Ruins & Castles ###

See 'mines_ruins_caves' in mods directory.


### Other Textures ###

See 'other' in mods directory.


### Character & NPC ###

- Total Character Makeover (for beast races)

- UNP Female Body Renewal - A female face and body replacer

- SkySight Skins - Ultra HD 4K 2K Male Textures and Real Feet Meshes

- Improved Eyes Skyrim

- Beards

- Bed Head - A Vanilla Hair Replacement

- Superior Lore-Friendly Hair - HD textures

- Realistic Hair Colors

- PAINTERLY - a High Res Vanilla Warpaint Retexture (Oldrim)

- RS Children Overhaul

- Bijin NPCs SE

- Bijin Wives SE

- Bijin Warmaidens SE


### Creature Textures ###

- Bellyaches Animal and Creature Pack SSE

- Diverse Dragons Collection SE (DDCse)

- DRAGON PRIEST

- DRAUGR

- ElSopa HD - Strider And Netches SE

- FALMER

- GIANT

- HAGRAVEN

- HD Werewolf Retexture

- MAMMOTH

- RUSTIC DAEDRA - Special Edition

- RUSTIC FROSTBITE SPIDER - Special Edition

- RUSTIC SPRIGGAN - Special Edition

- RUSTIC DEATH HOUND and GARGOYLE - Special Edition

- RUSTIC DRAGON CORPSE - Special Edition

- SABRECAT

- SKELETON

- TROLL

- Vampire Lord Retexture

- WISPMOTHER

- 2-4k Highland Cow Retexture


### Armor and Clothing ###

- Ars Metallica - Smithing Enhancement

- [CC's HD Daedric Weapons and Armor](https://www.nexusmods.com/skyrimspecialedition/mods/23029)

- [CC's HD Dwemer Weapons and Armor](https://www.nexusmods.com/skyrimspecialedition/mods/32384)

- [CC's UHD Stalhrim Weapons and Armor](https://www.nexusmods.com/skyrimspecialedition/mods/27205)

- Frankly HD Dawnguard Armor and Weapons

- Frankly HD Masque of Clavicus Vile

- Frankly HD Miraak

- Frankly HD Nightingale Armor and Weapons

- Frankly HD Shrouded Armor

- Immersive Armors

- RUSTIC ARMOR and WEAPONS SE

- RUSTIC FORSWORN - Special Edition

- RUSTIC CLOTHING - Special Edition


### Weapons ###

- Auriel's Shield HD

- Belt-Fastened Quivers

- Frankly HD Dragonbone and Dragonscale - Armor and Weapons

- LeanWolf's Better-Shaped Weapons SE

- Skyforge Weapons SSE

- Skyrim SE Expanded Skyrim Weaponry

- Staff of Magnus HD

- Unique Uniques SE

- Weapons of the Third Era SSE


### AI Improvements ###

- Amazing Follower Tweaks SE

- Immersive Citizens - AI Overhaul SE

- Immersive Patrols SE

- Run For Your Lives


### Gameplay Improvements ###

- Acquisitive Soul Gems Multithreaded

- Unleveled Items


### Combat ###

- Apocalypse - Magic of Skyrim

- Archery Gameplay Overhaul SE

- No BS AI Projectile Dodge (Magic and Arrows) - Immersive Projectiles Nondetection of Enemies

- No Spinning Death Animation

- Ordinator - Perks of Skyrim

- Realistic Ragdolls and Force

- TK Dodge SE

- Ultimate Dragons SE

- Ultimate Combat SE

- Wildcat - Combat of Skyrim

- 3PCO - 3rd Person Camera Overhaul - Smooth Camera Follow


### Quest ###

- Beyond Skyrim - Bruma SE

- Clockwork (SSE)

- Darkend

- Fuz Ro D-oh - Silent Voice

- The Forgotten City

- The Paarthurnax Dilemma

- QUASIPC - Qwinn's Unified Automated Self Installing Patch Compendium

- Stones of Barenziah Quest Markers


### Immersion ###

- Blowing in the Wind

- Footprints

- Immersive HUD - iHUD Special Edition

- Lanterns of Skyrim SE

- Wet and Cold


### Audio ###

- Immersive Sounds - Compendium


### LOD ###

- HD LODs Textures SE

- Indistinguishable Billboards for Skyrim SE

- Terrain LOD redone



## DynDOLOD ##

1. Disable any mods that add trees to cities.

2. Download the latest DynDOLOD Resources SE and the Standalone files.

3. Extract DynDOLOD Standalone to the location you keep the rest of your
   modding tools.

4. If needed, add DynDOLODx64.exe and TexGenx64.exe to your mod manager's
   executables with the -sse argument.

5. Install all files in the LOD section above along.

6. Install DynDOLOD Resources SE with your mod manager, selecting the options
   of your choice.

7. Ensure the new mod listing is activate in your mod manager and is the last
   mod in your mod list.

8. Install 3D Trees and Plants along with the BILLBOARDS, optional file (let
   it overwrite DynDOLOD Resources SE files).

9. Run TexGen with the default settings. Compress the output and install it
   via mod manager. Place it last on the mod list.

10. Run DynDOLOD.

11. Most users can keep the defaults here, select the worldspaces to run
    (usually all of them), and simply click a preset to run. Advanced users
    can click the wizard to have access to run DynDOLOD to generator only
    specific things or include additional features like Candles, FX Glow
    Lights, and Windows.

12. Once DynDOLD finishes, Save and Exit, and install the output to a new mod
    using your mod manger.

13. Active the new mod and sort your load order. Don't forget to reactivate
	any mods that add trees to cities. Done!
