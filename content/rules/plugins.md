---
title: "Plugins Utilized"
description: "A quick reference guide to plugins the server uses"
categories: ["rules", "guide"]
showToc: false
showShare: false
layout: legal
---

In this server, there are a couple important plugins that the server utilizes in order to elevate the vanilla surivival experience. Below is a list of the plugins, a quick reference on how to use them, and a link to more documentation.

- [Geyser](#geyser)
- [Dynmap](#dynmap)
- [Simple Voice Plugin](#simple-voice-plugin)
- [Skoice](#skoice) - *Deprecated*

## Geyser

Geyser self describes itself on their website [here](https://geysermc.org/) as follows:

>Geyser is a proxy, bridging the gap between Minecraft: Bedrock Edition and Minecraft: Java Edition servers. The ultimate goal of this project is to allow Minecraft: Bedrock Edition users to join Minecraft: Java Edition servers as seamlessly as possible to allow for true cross-platform.

While this is something that players won't directly interface with, we decided to put this up for transparency. Geyser will only be noticable to players when it stops working, notably around version updates. When this happens, the admins will wait in the Geyser official discord, and wait until the new version is released in order to fix the bedrock connections.

## Dynmap

Dynmap is essentially Google Maps for Minecraft, and can be accessed from your browser at [map.lorecraft.cc](http://map.lorecraft.cc).

Within Dynmap, you can claim land by claiming an area. Once you claim land, that land is yours to use  as you see fit. Below are some commands to help you get started with claiming an area:

1. Move to a corner or point on the outside of the area that you want to claim
2. Type `/dmarker add corner`
3. Move to the next point on the outside of the area that you want to claim, making a straight line from the last corner
4. Type `/dmarker add corner` again; this essentially draws a line between the first corner and this one.
5. Repeat steps 3 and 4 until you have outlined your area
6. After adding the last corner, type `/dmarker addarea {label}`, replacing the label with whatever you want to name the area

Congragulations! You have just claimed an area! This area now shows on the map. If you would like too (and we highly recommend that you do), change the outline color by doing `/dmarker updatearea {label} color:#{RRGGBB}`, or change the fill color with `/dmarker updatearea {label} fillcolor:#{RRGGBB}`. You can even change the opacity by doing `/dmarker updatearea {label} fillopacity:{0.0-1.0}`, where 0 is transparent and 1 is completely filled.

You can also add individual icons to the map as well. This could be for shops, or whatever you like! You can add a marker to the map by doing `/dmarker addicon id:{ID} {label} icon:{icon}`. The list of icons that you can choose from can be found below:

![image](https://camo.githubusercontent.com/564f8e6e4f240bcb3dd14876b4de0ccf5535fc3117e7160924c46eeb895152bf/687474703a2f2f6d696b657072696d6d2e636f6d2f696d616765732f4d61726b6572732e706e67)

Want to dive even deeper in Dynmap? Their wiki can be found at [this link](https://github.com/webbukkit/dynmap/wiki/Using-Markers).

## Simple Voice Plugin

"Simple Voice Chat" is a proximity voice chat system that doesn't rely on discord, but instead is fully used and operated within Minecraft. It's even the same one used in HermitCraft!

Below you will find instructions for if you're using [ATLauncher](https://atlauncher.com/) (trail's personal favorite launcher), or if your using the normal launcher. I recommend you use ATLauncher or an alternative that makes it easy to update mods, but that choice is up to you.

### SVP with ATLauncher

1. If you don't already have a modded instance:
    1. Go to "Create Pack"
    2. Click the latest version, and select "Fabric" as the loader. Then, click "Create Instance"
    3. Go to the instances page and select "Add Mods"
    4. Download the Fabric API by selecting the button under the search bar in the top right.
2. Search for "Simple Voice Chat" in the "Add Mods" section
3. *Optional* - Search for and install "Mod Menu" (I have the best luck locating it in Modrinth)

That's all! Go ahead and launch your game, and you should see a little icon in the bottom right, that means it's working! You can use the "V" button to look at what's going on (if you have other mods, you may need to bind this to a different key).

### SVP without ATLauncher

1. Go to the [Simple Voice Chat mod on Curseforge](https://www.curseforge.com/minecraft/mc-mods/simple-voice-chat) and download the latest fabric version of the mod.
2. Go to the [Fabric MC Website](https://fabricmc.net/) and download for windows.
    - If you are playing on Mac/Linux, download the universal jar located directly below the button.
3. On Windows, use the Fabric installer you downloaded to download it - *ensure you use the same version as the mod you downloaded*
4. Open the Microsoft launcher, and select the "Fabric Loader" installation and "Play"
5. Now go to "Run" and type: `%appdata%`
    - You can also press the Windows Key (⊞) + R key to open the Run box
6. Then go to `Roaming/.minecraft/mods`
    - If this doesn't show up, just make a folder in .minecraft called "mods"
7. Drag the Java file for the mod into this folder
8. Start minecraft!


{{<youtube mjblVOTJz2Y>}}


[^1]: https://www.curseforge.com/minecraft/mc-mods/simple-voice-chat
- [Fabric MC Website](https://fabricmc.net/)

## Skoice 

***Note: Skoice has now been deprecated by our server. Please utilize [Simple Voice Plugin](#simple-voice-plugin) for proximity chat***

Skoice is essentially in-game voice chat, that is powered by discord. It uses a custom-built discord bot, along with a plugin to the server, in order to tell your position to other players, and if you are within 50 blocks of another player, you will be put in a special voice chat.

There is some first time setup that you have to do in order to utilize the plugin. Follow below to get Skoice linked:

1. Join the minecraft server
2. Type `/link` in Discord
    - _Please utilize the #bots channel in discord, as most users have this muted_
3. You should receive a DM from Skoice with a code; copy the token from the DM
4. With your player in the server, type `/skoice link {token}`
5. Congrats! You've linked your skoice and minecraft account!

Now, to utilize the proximity voice chat, join the __local__ voice chat. Skoice will mute you as soon as you join. If you get close to another player also in local, Skoice will move you to a freshly created voice chat, and unmute you both so you can chat! Once out of proximity again, Skoice will mute you and move you back to the local voice chat.

Want to learn more? Visit the original github page [located here](https://github.com/Skoice/skoice) for the Skoice Project.