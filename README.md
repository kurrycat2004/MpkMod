# MPK Mod
[![Discord](https://img.shields.io/discord/819737524372504587?color=7289DA&logo=discord)](https://discord.gg/rSzmsdXsvW)

***This version of MPK Mod will no longer be updated and is replaced by [MPK Mod 2](https://github.com/kurrycat2004/MPKMod_2)***

MPK Mod is a minecraft mod for 1.8.9/1.12 that adds some features for [minecraft parkour](https://www.mcpk.wiki/wiki/Main_Page) to your client. It's a client side only mod, that means it can be used on any server.

## Content
- [Installation](#Installation)
- [FAQ](#FAQ)
- [Commands](#Commands)

### Installation

To install MPK Mod you need to have [forge](https://files.minecraftforge.net) installed.
To use the Mod you have to download the file `mpkmod-X.X.X.jar` (or `mpkmod-X.X.X-MC1.12` for minecraft 1.12-1.12.2)<sup>[1](#footnote1)</sup> from [releases](https://github.com/kurrycat2004/MpkMod/releases) and put it into your `mods` folder which is located in [`.minecraft`](https://minecraft.gamepedia.com/.minecraft).

### FAQ
##### **How do I change the UI color?**<br/>
The primary color can be changed with `/mpk color1 [color]` and the secondary one with `/mpk color2 [color]`

##### **How do I enable offset being sent in chat?**<br/>
To enable this feature and some others you have to change the setting in the config file located at `.minecraft/config/mpkmod.cfg`. If the setting is set to `true` it means that the setting is turned on and if it's set to `false` the setting is disabled. This specific setting is named `sendOffsetInChat` and is `false` by default. After updating something in the config file you can reload it with `/mpk reloadconfig` or by restarting your game.

### Commands
All commands are accessible with the `/mpk` prefix.
|Command|Syntax     |Explanation|
|-------|-----------|-----------|
|`anticp`|`/mpk anticp`|Turns anticp on/off|
|`clearlb`|`/mpk clearlb`|Clears the saved landing block|
|`clearmaxspeed`|`/mpk clearmaxspeed`|Clears the Max Speed label value|
|`clearpb`|`/mpk clearpb`|Clears the PB value|
|`color1`|`/mpk color1 [color]`|Changes the primary UI color to the specified `color`|
|`color1`|`/mpk color2 [color]`|Changes the secondary UI color to the specified `color`|
|`colorlist`|`/mpk colorlist`|Sends a list of all available colors in chat|
|`config`|`/mpk config`|Opens the config GUI where mod settings can be changed|
|`df`|`/mpk df [int]`|Specifies a new coord precision value that can range between 0 (no decimals) and 16 (16 decimals)|
|`gui`|`/mpk gui`|Opens a GUI for positioning the labels as well as disabling and removing them|
|`help` |`/mpk help`|The most basic command that displays a list of all commands and a short explanation for each one in chat<sup>[2](#footnote2)</sup>
|`macro`|`/mpk macro gui\|run\|stop`|A command for opening the macro gui, running<sup>[3](#footnote3)</sup> the macro or stopping it|
|`reloadconfig`|`/mpk reloadconfig`|Reloads the config file|
|`resetgui`|`/mpk resetgui`|Resets the color, position and enabled/removed state of every label. **Warning! Doing this will clear all previously saved gui settings**|
|`setcond`|`/mpk setcond [xmin] [xmax] [zmin] [zmax]`|Sets a landing condition|
|`setlb`|`/mpk setlb [(optional) x\|z\|~] [(optional) [[target]\|[x y z]]`|Sets the landing block. For example `/mpk setlb` without arguments just sets the landing block to the block you are standing on while measuring both X and Z offsets when attempting the jump. To just measure one of the X and Z offset just specify it as first argument. `/mpk setlb x` would only measure the offset on the X axis. You can also do `/mpk setlb ~` to use the axis you are currently looking as argument. To specify an other block than the one you are standing on you can do `/mpk setlb x y z` with `x`, `y` and `z` being the coordinates of the block. To specify the block you are looking at as landing block you can do `/mpk setlb target`|
|`timer`|`/mpk timer toggle\|reset`|Toggles or resets the Timer|
|`toggleall`|`/mpk toggleall`|Shows/Hides all labels|
|`togglesprint`|`/mpk togglesprint`|Turns togglesprint on/off|

<a name="footnote1">1</a>: For version 1.2.5 and higher the same jar file (`mpkmod-X.X.X.jar`) can be used for 1.8 and 1.12 and therefore only one jar file can be downloaded.</br>
<a name="footnote2">2</a>: All messages displayed in chat that have the prefix `<MPK>` are only visible to you.</br>
<a name="footnote3">3</a>: Macros can only be executed in SinglePlayer to prevent players from cheating on servers.
