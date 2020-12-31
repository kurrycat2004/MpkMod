# MPK Mod

MPK Mod is a minecraft mod for 1.8.9/1.12 that adds some features for [minecraft parkour](https://www.mcpk.wiki/wiki/Main_Page) to your client. It's a client side only mod, that means it can be used on any server.

## Content
- [Installation](#Installation)
- [FAQ](#FAQ)
- [Commands](#Commands)

### Installation

To install MPK Mod you need to have [forge](https://files.minecraftforge.net) installed.
To use the Mod you have to download the file `mpkmod-X.X.X.jar` (or `mpkmod-X.X.X-MC1.12` for minecraft 1.12-1.12.2) and put it into your `mods` folder which is located in [`.minecraft`](https://minecraft.gamepedia.com/.minecraft).

### FAQ
> **How do I change the UI color?**<br/>
> The primary color can be changed with `/mpk color1 [color]` and the secondary one with `/mpk color2 [color]`

> **How do I enable offset being sent in chat?**<br/>
> To enable this feature and some others you have to change the setting in the config file located at `.minecraft/config/mpkmod.cfg`. If the setting is set to `1` it means that the setting is turned on and if it's set to `0` the setting is disabled. This specific setting is named `sendOffsetInChat` and is `0` by default. After updating something in the config file you can reload it with `/mpk reloadconfig`.

### Commands
All commands are accessible with the `/mpk` prefix.
|Command|Syntax     |Explanation|
|-------|-----------|-----------|
|`help` |`/mpk help`| The most basic command that displays a list of all commands and a short explanation for each one in chat<sup>[1](#myfootnote1)</sup>
|`colorlist`|`/mpk colorlist`|Sends a list of all available colors in chat|
|`color1`|`/mpk color1 [color]`|Changes the primary UI color to the specified `color`|
|`color1`|`/mpk color2 [color]`|Changes the secondary UI color to the specified `color`|
|`gui`|`/mpk gui`|Opens a GUI for positioning the labels as well as disabling and removing them|
|`df`|`/mpk df [int]`|Specifies a new coord precision value that can range between 0 (no decimals) and 16 (16 decimals)|
|`setlb`|`/mpk setlb [(optional) x\|z\|~] [(optional) [[target]\|[x y z]]`|Sets the landing block. For example `/mpk setlb` without arguments just sets the landing block to the block you are standing on while measuring both X and Z offsets when attempting the jump. To just measure one of the X and Z offset just specify it as first argument. `/mpk setlb x` would only measure the offset on the X axis. You can also do `/mpk setlb ~` to use the axis you are currently looking as argument. To specify an other block than the one you are standing on you can do `/mpk setlb x y z` with `x`, `y` and `z` being the coordinates of the block. To specify the block you are looking at as landing block you can do `/mpk setlb target`|
|`clearlb`|`/mpk clearlb`|Clears the saved landing block|
|`clearpb`|`/mpk clearpb`|Clears the PB value|
|`resetgui`|`/mpk resetgui`|Resets the color, position and enabled/removed state of every label. **Warning! Doing this will clear all previously saved gui settings**|
|`setcond`|`/mpk setcond [xmin] [xmax] [zmin] [zmax]`|Sets a landing condition|

<a name="myfootnote1">1</a>: All messages displayed in chat that have the prefix `<MPK>` are only visible to you.
