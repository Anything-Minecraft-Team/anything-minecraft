# Vanilla JAR

## Overview

Vanilla is the original server jar that is distributed by Mojang.
Plugins and mods are not supported on this.
Vanilla servers behaves like normal Singleplayer Minecraft.
Minecraft has a simple config called `server.properties` which you can use to change some basic settings.
Some of the main settings are, `motd=A Minecraft Server`, this changes what is displayed under your server in the server list, `max-players=20`, this changes the max amount of players that can join the server at once, `view-distance=10`, this changes the max render distance you can set, on the client you can set it to a higher value but it wont display that far, and many more! To see the default config go [here](https://github.com/Anything-Minecraft-Team/anything-minecraft/blob/fork-info/resources/DEFAULT/server.properties).

Suggested version: It's suggested you use this for any Minecraft version if you don't mind having any vanilla glitches, bugs or bad performance.

## Information

Everything is the same as vanilla Minecraft with LAN open.

### Commands

Here is a good page on [vanilla commands](https://minecraft.gamepedia.com/Commands).

### Config

Here you will learn what each config option does. For an example of the `server.properties` file go [here](https://github.com/Anything-Minecraft-Team/anything-minecraft/blob/fork-info/resources/DEFAULT/server.properties).

`allow-flight` - Allows players to fly while in survival with a fly hack/mod without getting kicked. Defaul value `true`. Recommended value `true`.

`allow-nether` - Sets if players can travel to the nether.

`broadcast-console-to-ops` - Sets if the console output is sent to online operators.

`broadcast-rcon-to-ops` - Sets if online operators receive rcon commands.

`difficulty` - Sets the difficulty for the world.

`enable-command-block` - Sets if command blocks are allowed to run commands.

`enable-query` - Sets if the GameSpy4 protocal server listener is enabled. Used to get information about the server.

`enable-rcon` - Sets if remote access to the console is enabled.

`enable-status` - Sets if the server displays as offline or online in the server list, still allows connections.

`enforce-whitelist` - Sets if the whitelist is enforced on the server.

`entity-broadcast-range-percentage` - Sets how close entities need to be before they are rendered on the client.

`force-gamemode` - Sets if the players gamemode is forcefully set to the `gamemode` value when they join.

`function-permission-level` - Sets default permission level for functions.

`gamemode` - Sets the default gamemode for players to join with.

`generate-structures` - Sets if the world generates structures such as villages.

`generator-settings` - Sets the settings for custom world generation.

`hardcore` - Sets if the whole server to hardcore mode, forces the difficulty to hard.


`level-name` - Sets the name of the worlds, example, `world` or `world_the_end`.

`level-seed` - Sets the seed for the world to generate, if left blank it generates a random seed.

`level-type` - Sets the level type for the world, also used to generate custom terrain with mods like TerraForged.

`max-build-height` - Sets the max build height possible, 256 is the highest it can be set. Must be a multiple of 8.

`max-players` - Sets the max amount of players that can be in the server at once.

`max-tick-time` - Sets the maximum number of milliseconds a single tick may take before the server watchdog stops the server with the message.

`max-world-size` - Sets the size of the world.

`motd` - Sets what's displayed in the server list below the server name.

`network-compression-threshold` -

`online-mode` - Sets if the server checks connecting players against the Minecraft database. Setting this to false lets people with an unlicensed version of Minecraft, This also allows you to connect to the server with no internet connection.

`op-permission-level` - Sets what permission level players with op have.

`player-idle-timeout` - Sets how many minutes the player can be AFK for before getting kicked.

`prevent-proxy-connections` - Sets if players are kicked if the ISP/AS sent from the server is different from the one from Mojang Studios' authentication server.

`pvp` - Sets if pvp is enabled for the server.

`query.port` - Sets the port for the query server.

`rate-limit` - Sets the amount of packets the client can send before they are kicked.

`rcon.password` - Sets the password for RCON.

`rcon.port` - Sets the RCON network port.

`resource-pack-sha1` - Sets optional SHA-1 digest of the resource pack, in lowercase hexadecimal. It is recommended to specify this, because it is used to verify the integrity of the resource pack.

`resource-pack` - Sets the resource pack the player downloads to use on the server when joining. Must be a URI.

`server-ip` - Sets if the server is bind to a certain IP.

`server-port` - Sets the port the server runs on.

`snooper-enabled` - Sets if the server sends snoop data.

`spawn-animals` - Sets if animals can spawn.

`spawn-monsters` - Sets if monsters can spawn.

`spawn-npcs` - Sets if villagers can spawn.

`spawn-protection` - Sets how big the spawn protection area is.

`sync-chunk-writes` - Sets if synchronous chunk writes is enabled.

`text-filtering-config` - No info.

`use-native-transport` - Sets if Linux server performance improvements are enabled.

`view-distance` - Sets the max distance of chunks the player can view.

`white-list` - Sets if the whitelist is enabled.