# Skyrim SE Modding Guide #


## Preparation ##


### Clean Skyrim SE Installation ###

- Avoid installation on _C:\\_ drive if possible. If _C:\\_ is the only 
  option, install anywhere except _Program Files_.

- Disable Steam automatic updates and the Steam overlay.

- Start game and select ultra preset if auto-detect fails and then load into 
  the main menu. This is done in order to generate _.ini_ settings files.



### Mod Manager Installation ###

- Mod Organizer 2 (MO2) is the community favorite, download and run the 
  installer from Nexus.

- The installer should create a start menu shortcut. Right click this shortcut 
  and follow _More > Open file location > Shortcut > Advanced..._ and check 
  the _Run as administrator_ checkbox.

- Point mod manager to a new folder with **write permissions** for all mods 
  installed by the manager.



### LOOT Installation ###

- Download LOOT (Load Order Optimization Tool) from Nexus and run the 
  installer.
  
- LOOT should auto detect your game and flag _Update.esm_, _Dawnguard.esm_, 
  _HearthFires.esm_, and _Dragonborn.esm_ as dirty plugins.



### Clean Master Files ###

1. Download SSEEdit standalone.

2. Add _SSEEdit.exe_ and _SSEEditQuickAutoClean.exe_ executables to mod 
   manager.
   
3. Run _SSEEditQuickAutoClean.exe_ on each plugin individually in the 
   order below. The message "Background Loader: finished" should appear once 
   the plugin cleaning is complete.
   
   a. _Update.esm_
   
   b. _Dawnguard.esm_
   
   c. _HearthFires.esm_
   
   d. _Dragonborn.esm_
   
4. Create a new archive with the cleaned plugins so that updates to do not 
   revert them back to their old dirty state. Navigate to the Skyrim base 
   folder and add all 4 plugins above to an archive. Move the archive out of 
   the Skyrim data folder and install manually via MO2.



## SKSE Installation ##

- Download and extract the latest version.

- Copy both _.dll_ files and _skse64_loader.exe_ to Skyrim's base folder. 
  Create a shortcut in MO2 to _skse64_loader.exe_ and launch the game with 
  this from now on for SKSE to properly work.

- Send the _Scripts_ folder, located inside of the _Data_ folder, to a 7zip 
  archive and install manually via MO2.



## Core Mods ##

- Achievements Mods Enabler

- A Quality World Map

- Alternate Start - Live Another Life

- Cutting Room Floor

- PapyrusUtil SE - Modders Scripting Utility Functions

- SSE Engine Fixes (skse64 plugin)

- SkyUI

- Static Mesh Improvement Mod - SMIM

- Unofficial Skyrim Special Edition Patch



## ENB ##

1. Download and extract the enb binaries from 
   [enbdev](http://www.enbdev.com/download_mod_tesskyrimse.html)
   
2. Copy and paste _d3d11.dll_ and _d3dcompiler_46e.dll_ to Skyrim's base 
   folder.
   
3. Download and extract the enb of your choice from Nexus and follow the 
   author's installation instructions. Most enbs can be installed by simply 
   copying _enbseries_, _enblocal.ini_, & _enbseries.ini_ to Skyrim's base 
   folder, but some will have other dependencies (patches, weather mods, etc.)


### Additional ENB Mods ###

- ENB Helper SE

- [Skyrim particle patch for ENB](http://enbseries.enbdev.com/forum/viewtopic.php?f=6&t=1499)

- ENB Light (^Particle patch required. Let ENB light overwrite the patch files)

- NightEyeENBFix



## My Mod List ##


### Large Texture Packs ###

**Listed in load order**

1. Enhanced textures detail (UV-tweaks)

2. SSE Texture Pack - Osmodius

3. Noble Skyrim Mod HD-2K

4. Skyrim 2018 by Pfuscher Skyrim

5. Skyrim 2019 by Pfuscher

6. 2020 Textures by Pfuscher


### Weather, Lighting & Atmosphere ###

- Embers HD

- Enhanced Lights and FX

- ETHEREAL CLOUDS - Special Edition

- ETHEREAL COSMOS - Special Edition

- Fluffy Snow

- Just Ice

- Obsidian Weathers and Seasons

- Smooth Sky mesh - SSE

- Ultimate HD Fire Effects SSE


### Landscape ###

- Majestic Mountains - Cathedral Concept (with lods)

- Skyrim 3D Landscapes

- Skyrim 3D Rocks


### Clutter ###

- Forgotten Retex Project

- High Poly Project

- Misc Retexture Project

- Rudy HQ - Misc SE - The Rest

- Ruins Clutter Improved

- RUSTIC CLUTTER COLLECTION - Special Edition


### Cities ###

- Frankly HD Markarth - The White City Redux

- JK's Skyrim

- Leafeater's Whiterun Tree Overhaul SE


### Other Textures ###

- Arri's Snow Elf Ruins Retexture Special Edition

- Ash Pile Retexture

- Astral Aspect - 4K Standing Stones

- Barenziah's Glory SE

- BetterFalmerCaveCeilingGlow

- Blended Roads

- Book Covers Skyrim

- CC's HQ Barset

- CC's HQ Buckets

- CC's HQ Carts

- CC's Enhanced Ore Veins SSE Edition

- CC's HQ Guard Shields SSE

- CC's HQ Firewood

- CC's HQ Roadsigns SSE

- CL's Barrels and Crates

- ElSopa HD - Unique Hand Made Signs Overhaul SE

- Enhanced Blood Textures SE

- Ennead - Septims

- Farmhouse Door 3D

- Fences of Skyrim - No more flickering fences

- Gecko's Dwarven Ruins Textures

- Gemling Queen Jewelry SE

- Glorious Dwarven Metal

- Glorious Solitude Door Replacer SE

- HD Lava for Dawnguard

- JS Dragon Claws SE

- Low Resolution Particles

- Medieval Candlehorns and Sconces

- Medieval Silverworks

- Organic Riften Leaves

- PELTAPALOOZA - Special Edition

- Rudy HQ - Hay SE

- RUGNAROK - Special Edition

- RUSTIC ANIMATED POTIONS and POISONS

- RUSTIC AZURA'S STAR - Special Edition

- RUSTIC COOKING - Special Edition

- RUSTIC ELDERSCROLL - Special Edition

- RUSTIC FURNITURE - SPECIAL EDITION

- RUSTIC SOULGEMS - Special Edition

- RUSTIC WINDOWS - Special Edition

- Skyrim Textures Redone - SkyHaven

- Skyrim 3D Docks and Boardwalks

- Skyrim 3D Windmill

- Soul Cairn HD

- Soulgem Stand Redone

- Sovngarde HD

- Stalhrim Source

- Stunning Statues of Skyrim

- Training Dummies Retexture 4k and 2k

- Underground - a dungeon texture overhaul


### Mines & Ruins ###

- CC's Castle Volkihar Reborn

- CC's Fort Dawnguard Reborn

- Rudy HQ - Nordic Ruins SE


### Vegetation ###

- HD Photorealistic Ivy

- Skyrim 3D Trees and Plants

- Skyrim 3D Landscapes

- The Elder Scrolls - Veydosebrom - Grass and Groundcover


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

- Smoking Torches and Candles

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