# vpIZY_weapons_IzP_LBDR-compat-patch

## Introduction

This is a mod for the game [7 Days to Die](https://store.steampowered.com/app/251570/7_Days_to_Die/) that aims to make the [IZY-All in One Gun Pack v5.1](https://www.nexusmods.com/7daystodie/mods/5458) mod compatible with IzPrebuilt's [Learn By Doing Returns](https://www.nexusmods.com/7daystodie/mods/8642) ("LBDR") mod.  

**It is currently a work-in-progress.**

## Current state

### Known Issues

* new schematics need to be added to loot, traders(?), and Localization
* some schematics unlock crafting of items that don't have a recipe and should probably be disabled
* there is no Localization for existing LBDR perks, so you won't be able to tell in the skills window that, for example, investing in the 7.62 crafting perk also unlocks crafting 5.56 ammo.
* some of the IZY mods are not yet supported at all (see below)

### Supported Mods

The IZY AIO pack contains several mods in the zip file you download from Nexus.  This chart shows my progress of adding support for each of those mods, as well as a short description of their purpose or important assets included in them.

| MOD_ID         | SUP? | FOLDER (7D1.0_Izayo_ ...)     | DESCRIPTION             |
|-----------------|-----|-------------------------------|-------------------------|
| IZY_FPV_GLOVES    | X | Visible_FPV_Gloves_mod        | makes gloves visible in first-person view |
| IZY_MMVMV2        | X | Visible_Mods_mod              | buffs,kick,Notready_ICON,IZYadvancegunrepairkit |
| IZY_RMP_Miscpack  | X | WeaponpackMisc_pack           | Muskets, "Light" crossbow bolts, IZYgunT4BowVanhelsingAutomaticCrossbowVH |
| IZY_RMP_44magnum  | X | WeaponpackRemastered_44mag    | Magnums |
| IZY_RMP_45ACP     | X | WeaponpackRemastered_45ACP    | 45 ammo, handguns, smgs, rifles.  handgun/smg use 9mm tags/perks |
| IZY_RMP_556pack   | X | WeaponpackRemastered_556pack  | 556 ammo, rifles, machine guns.  uses 762 tags/perks |
| IZY_RMP_762pack   | X | WeaponpackRemastered_762pack  | sniper rifles, machine guns/ARs |
| IZY_RMP_9mmVAL    | X | WeaponpackRemastered_9mmVAL   | Handguns,SMGs |
| IZY_RMP_Demopack  |   | WeaponpackRemastered_DemolitionPack   | |
| IZY_RMP_HVW       |   | WeaponpackRemastered_Heavy_WeaponPack | |
| IZY_RMP_SG        | X | WeaponpackRemastered_SHOTGUNpackVAL   | Shotguns |
| IZY_RMP_Tech      |   | WeaponpackRemastered_Technicalpack    | |
| IZY_melee         |   | WeaponpackSpecial_Melee       | |
| IZY_VRP           | X | WeaponpackVanillaReplacer     | replaces T1-T3 shotguns, ARs, rifles, handgun/smgs |

## Installation

### Warning

Unless you know exactly what you're doing, you **should not install this mod** yet.  As stated at the top of this readme, this mod is a **work in progress**.  It is not my fault if you blow up your computer or corrupt your save game.  In it's current state, it's intended for testing ONLY.

Once the mod is complete, I will put up a page for it on [Nexus Mods](https://next.nexusmods.com/).  In the meantime, feel free to checkout my [other mods](https://next.nexusmods.com/profile/vinylplz/mods).  In particular, both the [Steel Fire Axe](https://www.nexusmods.com/7daystodie/mods/8603) and [LRS Weapons and IzP LBDR Compatibility Patch](https://www.nexusmods.com/7daystodie/mods/8711) mods have LBDR support.

### Requirements

* 7D2D v2.3 stable (2.4 is probably fine, but untested)
* IZY AIO v5.1
* IzP LBDR v1.2

### Steps

1. Install the IZY AIO 5.1 pack, and the Learn By Doing ("LBDR") mods as normal.
2. Download the latest "vpIZY_weapons_IzP_LBDR.compat.patch-vX.X.X.zip" zip file from the "releases" section on the right hand side of this page.
3. Extract the zipfile into your Mods directory
4. If any of the above is confusing to you, stop.  Wait for the actual release.
5. The IZY mods must be loaded prior to LBDR.  To accomplish this, we can rename them, prefixing them with "0_z ".  For convenience, I've included a powershell script to do this for you.  Just double click on the "rename_izy_folders.bat" file in the root folder of this mod.  It should list all of your installed IZY mod folders, and prompt for confirmation before renaming them.
6. Remove any of the IZY mods that do not have an "X" in the "SUP?" column of the above table.  Failure to do so can crash your game.  One easy way to do this is create a "_disabled" folder inside your Mods directory, then drag the not-yet-supported Mods into it.  Since they are two-levels deep, 7D2D will not see their ModInfo.xml, and will ignore them.
7. That's it.  Launch the game and check for errors.

## License

While there is no formal license for this (yet?), I ask that you do not upload a version of this to Nexus Mods or any other site (e.g. [7daystodiemods.com](https://7daystodiemods.com/)), *especially* before it's finished.  I'm providing the code for it here so people (like Izy) can see the current state/progress, as well as serving as an example for people that may want to develop LBDR support for other mods.

If a significant amount of time has passed where I'm not providing updates, especially if there are updates to IZY AOI or LBDR, you are welcome to fork the repo and release your own version on Nexus, provided that you get permission from Izayo prior to doing so, and attribute me as the original author.

Izayo (aka IZY), and IzPrebuilt, as the original authors of the mods on which this depends, are exempt from any such restrictions, and are welcome to copy any of the code from this mod into their own mods at any time, with or without attribution or further permission from me.

## Contact

The easiest way to get in touch with me is on the [Guppy's Unofficial 7DtD Modding Server](discord.gg/WpVPJWj7Xk).  Chances are good that, if you're reading this, you're already a member.  I don't have my own channel, so tagging `@vinylplz` in #7modders_general is probably your best bet.
