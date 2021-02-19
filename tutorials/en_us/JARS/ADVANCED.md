# Advanced JAR picking

If you want to go a little more in-depth with JAR picking, you've come to the right place.

## Server Software:

Server software is the software that allows multiple players to play on a server together.

### Plugins:

- [CraftBukkit](https://getbukkit.org/download/craftbukkit) - It's the BASE for all forks that are out today and they still are updating it to this day, not newbie friendly at all because it requires manual building (or you can get it [here](https://getbukkit.org)). The only real case of use is for minecraft versions from 1.0.0 to 1.4.5 as there is no spigot release for those versions.

- [Spigot](https://www.spigotmc.org/) - The original fork of Bukkit, improved performance vs CraftBukkit, still widely used, recommended alternative if for some reason you don't want to use PaperSpigot.

- [PaperMC](https://papermc.io/) - Most popular JAR for Spigot/Bukkit, quite fast and stable, they roll out small patches at least every two days or so, good choice if you're just starting with your MC server and don't have much past experience because it's fast and simple.

- [Tuinity](https://github.com/Spottedleaf/Tuinity) - PaperMC fork aimed at improving stability and performance at high player counts.

- [Purpur](https://purpur.pl3x.net/) - It's a fork of both PaperSpigot and Tuinity to deliver very fast performance with stability for high player counts and it adds a lot of custom features that aren't seen on any other forks.

- [Airplane](https://github.com/TECHNOVE/Airplane) - This fork includes optimizations oriented towards large servers. 

- [Purplane](https://github.com/notOM3GA/Purplane) - A fork of purpur that adds features from [Airplane](https://github.com/TECHNOVE/Airplane).

- [SpongeVanilla](https://www.spongepowered.org/downloads/spongevanilla) - A server implementing the Sponge API, a different plugin API separate from the Bukkit API. This implementation also includes some general improvements regarding performance and server settings.

- [FoxSpigot](https://www.mc-market.org/resources/8592/)

- [Yatopia](https://github.com/YatopiaMC/Yatopia) - Aims to combine the code from many Paper forks and optimization mods, as well as many unique optimizations, but its known to be very unestable and usually Purpur is a better choice. Only use if you desperately need performance and think it's worth the instability. Yatopia has been known to corrupt data so keep daily backups.

### Mods:

- [Forge](http://files.minecraftforge.net/) - Forge is a server software based on the MCP. Both the server and client need to be running the mods.

- [Fabric](https://fabricmc.net/) - Fabric, unlike Forge, is not based on the MCP. This allows it to be updated for snapshots easier. It is incompatible with Forge.

### Plugins + Mods:

- [Magma](https://magmafoundation.org/) - Minecraft Forge Hybrid server implementing the Spigot/Bukkit API (Cauldron for 1.12)

- [Mohist](https://mohistmc.com/) - Minecraft Forge Hybrid server implementing the Paper/Spigot/Bukkit API(1.12.2/1.16), formerly known as Thermos/Kettle/Cauldron/MCPC+

- [Arclight](https://github.com/IzzelAliz/Arclight) - A Minecraft Bukkit(1.15/1.16) server implementation on Forge using Mixin

- [SpongeForge](https://www.spongepowered.org/downloads/spongeforge) - SpongeForge allows both SpongeVanila plugins as well as Forge mods on one server.

## Network Software:

- [BungeeCord](https://www.spigotmc.org/wiki/bungeecord/) - Base for the Waterfall fork, these JARs are used for configuring networks of which an example is Hypixel or Mineplex, it is used for distributing
  workload and players to different lobbies (are actually different server instances run with seperate files and data).
  No, this can't be used as a normal JAR and requires at least 3 servers/instances, one is BungeeCord (or it's fork) which is called the proxy, players
  connect to this proxy and are sent to the default server which is set in config. Let's say server "Lobby" is default, it will send you there,
  after that you can connect to another server, for example "Survival" which is running in a seperate server/instance and BungeeCord enables the functionality
  travel across these different servers without returning back to the multiplayer menu screen.
  (It can be done with special plugins which utilize BungeeCord API to send you to the chosen server on click, you'll most commonly see it as the
  compass or a portal)
- [Waterfall](https://papermc.io/downloads#Waterfall) - Fork of BungeeCord, faster than BungeeCord and has general improvements and tweaks which make it the more preferred network JAR, works basically the
  same as BungeeCord (talking about the use, it doesn't have a different system).
- [Velocity](https://velocitypowered.com/) - A next-generation Minecraft proxy focused on scalability and flexibility. It allows server owners to link together multiple Minecraft servers so they may appear as one.
- [Travertine](https://github.com/PaperMC/Travertine) - Fork of Waterfall with added 1.7.10 support if you want that old school experience ;)