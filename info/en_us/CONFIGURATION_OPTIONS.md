# Configuring Your Server

There are many ways to configure your server, often depending on what JAR you're using. There are a few things that you can do with _any_ server jar, and that's what we'll show in this tutorial.

## Finding Your Configuration File

To find your server configuration file, you'll need to look in the root directory of your server (Where your server JAR is). After you've run your server for the first time, you should have a file called `server.properties`. This config file has many settings that you can change to modify your server.

## Configuration Options

**You can find the default `server.properties` [here](../../resources/default_server.properties) or on the [GitHub](https://github.com/JustDoom/anything-minecraft) if you accidently mess it up, or forget a setting's original value.**

### `enable-jmx-monitoring`

Exposes an MBean, or Managed Bean ([Read More](https://en.wikipedia.org/wiki/Java_Management_Extensions#Managed_beans)) with the Object name `net.minecraft.server:type=Server` and two attributes `averageTickTime` and `tickTimes` exposing the tick times in milliseconds

The default value is `false` and you should leave it there, unless a plugin or other service requests that you enable it.

### `rcon.port`

The port that you'll need to open inorder to connect with RCON(see [`enable-rcon`](#enable-rcon))

### `level-seed`

The seed that you want to use for world generation

After you do this, you'll need to remove the world file in the root directory of your server.

### `gamemode`

The gamemode for your server.

Possible Values: survival, creative, adventure, spectator

### `enable-command-blocks`

Should command blocks be allowed to run.

Note: Command blocks can only be placed by players with OP, but if there's a redstone signal to one, anybody can run it.

### `enable-query`

Enables GameSpy4 ([Read More](https://wiki.vg/Query)) protocol server listener. Used to get information about the server.

The default value is `false` and you should leave it there, unless a plugin or other service requests that you enable it.

### `generator-settings`

The settings used to customise world generation

Follow the format found [here](https://minecraft.gamepedia.com/Java_Edition_level_format#generatorOptions_tag_format)

### `level-name`

The name of your world folder in your root directory

### `motd`

The motd, or Message Of The Day is the message that displays under the name of the server in a client's server list.

By default, all text will be white. This colour can change through the use of colour codes in the format of `\u00A7` and then one of the sixteen colour codes and six formatting codes, or using the chart found below (the column titled 'MOTD code'). You can also you a [MOTD generator](https://mctools.org/motd-creator).

![Image of colour codes](https://lazerstudiozgaming.files.wordpress.com/2015/01/screen-shot-2015-01-03-at-11-27-44-am.png)

### `query.port`

The port for the query server (see [`enable-query`](#enable-query))

### `pvp`

Whether or not players can harm each other.

### `generate-structures`

Whether or not to generate structures like Villages, Strongholds, Outposts, and others

### `difficulty`

The difficulty of the server

Possible values: peaceful, easy, normal, hard

### `network-compression-threshold`

By default it allows packets that are n-1 bytes big to go normally, but a packet of n bytes or more gets compressed down. So, a lower number means more compression but compressing small amounts of bytes might actually end up with a larger result than what went in.

Note: The Ethernet spec requires that packets less than 64 bytes become padded to 64 bytes. Thus, setting a value lower than 64 may not be beneficial. It is also not recommended to exceed the MTU, typically 1500 bytes.

Possible values: Integer, -1 means disable compression entirely, 0 means compress everything

Default: 256

### `max-tick-time`

The max amount of milliseconds per tick before the server stops itself, assuming a crash has happened.

Possible Values: Integer 0 - 2⁶³-1

### `use-native-transport`

Linux server performance improvements: optimized packet sending/receiving on Linux

### `max-players`

Maximum players on at one time

### `online-mode`

When enabled, the server will assume that it has an internet connection and check all players joining for a valid Minecraft account.

### `enable-status`

Whether or not the server appears as 'online' in the server list

### `allow-flight`

When set to true, players who would normally be kicked for flying automatically will not be.

### `broadcast-rcon-to-ops`

Send rcon(see [`enable-rcon`](#enable-rcon)) console command outputs to all online operators.

### `view-distance`

The amount of world data the server sends the client. Value is measured in chunks

Possible Values: Integer (3-32)

### `max-build-height`

The maximum build height that someone can build.

Integer 0 - 256 (**must be multiple of 8**)
(as of 1.16.5)

### `server-ip`

The player should set this if they want the server to bind to a particular IP. This is most common if you have multiple IPs for a particular machine.

For almost all uses, this should be blank.

You can read into specific use cases [here](https://www.minecraftforum.net/forums/support/server-support-and/1920697-advanced-server-properties-ip-and-port-settings), if you believe that it may be necessary.

### `allow-nether`

Allow players to teleport to the Nether dimension

### `server-port`

The port that the server should be hosted on

### `enable-rcon`

Enables remote access([RCON](https://en.wikipedia.org/wiki/Remote_administration)) to the server console.

### `sync-chunk-writes`

Enables synchronous chunk writes.

### `op-permission-level`

Sets the default permission level for ops when using `/op`. All levels inherit abilities and commands from levels before them.

Possible Values:

1. Ops can bypass vanilla spawn protection
2. Ops can use all singleplayer cheats commands
3. Ops can use most multiplayer-exclusive commands
4. Ops can use all commands

### `prevent-proxy-connections`

If the ISP/AS sent from the server is different from the one from Mojang Studios' authentication server, the player is kicked

### `resource-pack`

URL to a resource pack

Note: In some versions before 1.15.2, the ":" and "=" characters need to be escaped with a backslash (\\)

### `entity-broadcast-range-percentage`

Controls how close entities need to be before being sent to the client. Higher values means they'll be rendered from farther away, potentially causing more lag.

Possible Values: Integer 0 - 500

### `rcon.password`

Password for rcon(see [`enable-rcon`](#enable-rcon))

### `player-idle-timeout`

The amount of minutes before a player is kicked from being idle

0 means that it will not kick

### `force-gamemode`

Force the player into the default gamemode(see [`gamemode`](#gamemode)) upon joining

### `rate-limit`

Sets the maximum amount of packets a user can send before getting kicked.

0 disables this feature.

### `hardcore`

When enabled, server [difficulty](#difficulty) is ignored, and set to hard. Players are set into spectator mode when they die.

### `white-list`

Should whitelist be enabled. Whitelist can be changed with the `whitelist.json` or in-game with `/whitelist`.

### `broadcast-console-to-ops`

Should console commands get broadcast to online Op players

### `spawn-npcs`

Whether or not villagers can spawn

### `spawn-animals`

Can animals spawn?

### `snooper-enabled`

Sets whether the server sends snoop data regularly to <http://snoop.minecraft.net>

This includes data about the version of Minecraft that you're running, hardware specs, Java version, JVM arguments, and generation settings. The full list can be found [here](https://wiki.vg/Snoop)

### `function-permission-level`

Sets the default permission level for functions. (See [`op-permission-level`](#op-permission-level))

Possible Values: Integer 1 - 4

### `level-type`

The type of map to generate

Possible Values: default, flat, largeBiomes, amplified, buffet(1.15+, settings set in [`generator-settings`](#generator-settings))

### `text-filtering-config`

Leave blank

### `spawn-monsters`

Should monsters spawn?

### `enforce-whitelist`

When this option is enabled, users who are not present on the whitelist (if it's enabled) get kicked from the server after the server reloads the whitelist file.

### `resource-pack-sha1`

Optional SHA-1 digest of the resource pack, in lowercase hexadecimal. It is recommended to specify this, because it is used to verify the integrity of the resource pack.

### `spawn-protection`

Determines the side length of the square spawn protection area as 2x+1.

Possible Values: Integer

0 - Disables spawn protection

### `max-world-size`

This sets the maximum possible size in blocks, expressed as a radius, that the world border can obtain.

Integer 1 - 29999984
