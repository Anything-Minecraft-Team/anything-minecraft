# Advanced JAR picking

If you want to go a little more in-depth with JAR picking, you've come to the right place.

## Server Software

Server software is the software that allows multiple players to play on a server together.

### Plugins:

- [CraftBukkit](https://getbukkit.org/download/craftbukkit) - It's the BASE for all forks that are out today and they still are updating it to this day, not newbie friendly at all because it requires manual building (or you can get it [here](https://getbukkit.org)). The only real use is for Minecraft versions from `1.0.0` to `1.4.5` as there is no Spigot release for these versions.  
Version: 1.0.0 - 1.16.5  
Currently Active

- [Spigot](https://www.spigotmc.org/) - The original fork of Bukkit, improved performance vs CraftBukkit, still widely used, recommended alternative if for some reason you don't want to use PaperMC.  
Version: 1.4.6 - 1.16.5  
Currently Active

- [PaperMC](https://papermc.io/) - Most popular JAR for Spigot/Bukkit, quite fast and stable, they roll out small patches frequently, so it is a good choice if you're just starting with your MC server and don't have much experience.  
Version: 1.7.10 - 1.16.5  
Currently Active

- [Tuinity](https://github.com/Spottedleaf/Tuinity) - PaperMC fork aimed at improving stability and performance at high player counts.  
Version: 1.13.2 - 1.16.5  
Currently Active

- [Purpur](https://purpur.pl3x.net/) - It's a fork of PaperMC with Tuinity and Airplane patches to deliver very fast performance with stability for high player counts and it adds a lot of custom features that aren't seen on any other forks.  
Version: 1.14.4 - 1.16.5  
Currently Active

- [Airplane](https://github.com/TECHNOVE/Airplane) - This fork includes optimizations oriented towards large servers.  
Version: ??? - 1.16.5  
Currently Active

- [Purplane](https://github.com/notOM3GA/Purplane) - A fork of purpur that adds features from [Airplane](https://github.com/TECHNOVE/Airplane). Purpur added Airplane patches and is now discontinued.  
Version: 1.16.5  
DISCONTINUED

- [SpongeVanilla](https://www.spongepowered.org/downloads/spongevanilla) - A server implementing the Sponge API, a different plugin API separate from the Bukkit API. This implementation also includes some general improvements regarding performance and server settings.  
Version: 1.8 - 1.12.2  
Currently Active

- [FoxSpigot](https://www.mc-market.org/resources/8592/) - FoxSpigot is a fork of Spigot aiming to make PvP server perform better.  
Version: 1.8.8  
Currently Active

- [Yatopia](https://github.com/YatopiaMC/Yatopia) - Aims to combine the code from many Paper forks and optimization mods, as well as many unique optimizations, but it's known to be very unstable and usually, Purpur is a better choice. Only use if you desperately need performance and think it's worth the instability.  
Version: 1.15.2 - 1.16.5  
Currently Active

- [Cuberite](https://cuberite.org/) - Cuberite is a server software developed in C++ and plugins are written in LUA. Cuberite is very lightweight and they also allow you to run a server on your android device! Cuberite is only 1.8-1.12, 1.13+ compatibility is being worked on.  
Version: 1.8 - 1.12.2  
Currently Active

- [Glowstone](https://github.com/GlowstoneMC/Glowstone) - Glowstone is a lightweight, from scratch, open-source Minecraft server written in Java that supports plugins written for the Bukkit API and its major forks, Spigot and Paper.  
Version: ???  
Currently Active

- [TacoSpigot](https://github.com/TacoSpigot/TacoSpigot) - A even-higher higher performance PaperSpigot fork that adds new features.  
Version: 1.8 - 1.10, 1.12  
Currently Active

- [SharperMC](https://github.com/SharperMC/SharperMC) - SharperMC is a C# 1.8.x Minecraft server running on the .NET Framework. SharperMC is a fork of [SharpMC](https://github.com/SharpMC/SharpMC) which was last updated in 2015.  
Version: 1.8.x  
Currently Active

- [MineStom](https://github.com/Minestom/Minestom) - MineStorm is an entire recode of Minecraft servers from the base up meant to remove all vanilla features. It removes features like the server understanding what a chest is, which allows HUGE performance increases for minigame servers as they may not need that feature. Every feature can be added back. Due to this, development would take longer and would not be suitable for survival servers.  
Version: ???  
Currently Active

- [Akarin](https://github.com/Akarin-project/Akarin/tree/ver/1.16.4) - A Spigot plugin compatible project aiming at becoming fairly multicore compatible. This is a fork of Tuinity aiming to simplify the logic and implement multi-threaded computing and make servers more safe and stable.  
Version: 1.13.2 - 1.16.5  
Currently Active

- AtomSpigot - A 1.8.8 TacoSpigot fork with crash fixes, async hit detection, and async knockback built it. Currently not available through legal means due to a false ban off of MCMarket.  
Version: 1.8.8  
DISCONTINUED

- DytanicSpigot - Other than its API it has been lost to time, but it was a Spigot fork said to be capable of stability hitting 40 TPS, although there's not much left of it to show if it was.  
Version: ???  
DISCONTINUED

- [xSpigot](https://www.mc-market.org/resources/11411/) - A 1.7.10 - 1.8.x TacoSpigot fork with custom knockback editing and options such as toggleable mob AI. This is meant for HCF servers and practice PvP servers.  
Version: 1.7.10 - 1.8.x  
DISCONTINUED

- ySpigot - ySpigot is a remake of xSpigot for later versions of Minecraft.  
Version: 1.7.10 - 1.12.x

- zSpigot - A 1.7.10 Paper fork with huge optimizations, completely custom knockback editing, built-in server benchmarking, and more PvP based features. Ironically, despite it originally being a premium resource the only way to get it now is through a leaks website due to the creator leaking resources.  
Version: 1.7.10  
DISCONTINUED

- [mSpigot](https://www.mc-market.org/resources/6864/) - Another premium TacoSpigot fork with promises of improved TNT and knockback aimed at PvP and Factions servers.  
Version: 1.8.8  
Currently Active

- [ImanitySpigot](https://www.mc-market.org/resources/10770/) - ImanitySpigot provides you with a better PvP experience with smooth hit detection, customizable knockback and projectile enhancements.  
Version: 1.8.8  
Currently Active

- [EmpireCraft](https://github.com/starlis/empirecraft) - EmpireCraft is a fork of Spigot used by the [Empire Minecraft Server](https://empireminecraft.com/lp/?user=Aikar&utm_campaign=Player%20Referrals&utm_source=github.com&utm_medium=Aikar). It contains many gameplay changes to suit the EmpireCraft server, but more importantly, contains new performance improvements pending testing to be contributed to Spigot / Paper / Sponge.  
Version: 1.9 - 1.13.2, 1.15.2 - 1.16.2  
Currently Active

- [Origami](https://github.com/Minebench/Origami) - Custom paper fork used by [Minebench.de](https://www.minebench.de/). The fork is based on the framework used in [Spottedleaf's Tuinity](https://github.com/Spottedleaf/Tuinity).  
Version: 1.14.4 - 1.16.5  
Currently Active

- [HOSE](https://github.com/softpak/HOSE) - MInecraft server with multi-thread computing.  
Version: 1.11.2  
DISCONTINUED

- [Cleanstone](https://github.com/CleanstoneMC/Cleanstone) - A multi-core design server jar coded from the ground up.  
Version: 1.12.2 - 1.14  
Currently Active

- [McEx](https://github.com/McEx/McEx) - McEx is a Minecraft server written in Elixir and Rust. All the networking and logic is implemented in Elixir, while the low-level chunk data handling is done in Rust.  
Version: ???  
DISCONTINUED

- [Lightstone](https://github.com/grahamedgecombe/lightstone) - The official server software has some shortcomings such as the use of threaded, synchronous I/O along with high CPU and RAM usage. Lightstone aims to be a lightweight and high-performance alternative.  
Version: ???  
DISCONTINUED

- [PerfectSpigot](https://www.mc-market.org/resources/5376/) - A 1.8.8 Paper fork focused on Factions servers with optimized cannoning and built-in world generators.  
Version: 1.8.8  
Currently Active

- [BeerSpigot](https://www.mc-market.org/threads/355569/) - A 1.8.8 TacoSpigot fork focused on Factions servers with a built-in knockback editing,  with a lot of built-in Factions features (Grace Period, Cannoning Optimization, and Setting Global Spawner Values).  
Version: 1.8.8  
Currently Active

- [BreadSpigot](https://www.mc-market.org/threads/475910/) - A 1.8.8 TacoSpigot fork focused on SkyBlock servers with huge entity optimizations, built-in mob stacking, and a built-in knockback editor.  
Version: 1.8.8  
Currently Active

- [ElapsedSpigot](https://www.mc-market.org/threads/480567/) - A 1.8.8 TacoSpigot fork focused on Factions servers with a built-in mob stacker, configurable block durabilities, huge factions based optimizations, and some vanilla feature toggles.  
Version: 1.8.8  
Currently Active

- [StellarSpigot](https://www.mc-market.org/threads/523827/) - A 1.8.8 TacoSpigot fork with a huge assortment of features and optimizations aimed at Factions servers.  
Version: 1.8.8  
Currently Active

- TorchSpigot - The now abandoned predecessor to Akarin based on a goal of getting Paper to run on multiple threads.  
Version: ???  
DISCONTINUED

- [APOLLO16 ](https://www.mc-market.org/resources/16271/) - A 1.16.5 Purpur fork with a built-in system monitor and optimized block and chunk ticking methods.  
Version: 1.16.5  
Currently Active

- [LightSpigot 1.8.8](https://www.mc-market.org/resources/16933/) - A free 1.8.8 Spigot fork focused on adding some optimizations and features for HCF servers, like enderpearls teleporting through slabs.  
Version: 1.8.8  

- [LightSpigot 1.16.5](https://www.mc-market.org/resources/17753/) - A 1.16.5 Spigot fork with some spawner / general performance optimizations and custom knockback editing.  
Version: 1.16.5  

- [VoltaneSpigot](https://www.mc-market.org/threads/571429/) - A 1.8.8 based TacoSpigot fork with built-in 1.7 - 1.16 client support with multi-thread support, custom knockback editing, discord server integration, and a lot of factions based features.  
Version: 1.8.8  

- [SSSpigot](https://www.mc-market.org/resources/14122/) - A 1.16.5 Paper fork with multi-thread support, useless code removal, some general optimizations, and tracking metrics disabled.  
Version: 1.16.5  

- [RocketMC](https://www.mc-market.org/resources/13898/) - A 1.15.2 Tuinity fork with a built-in monitoring system, plugin manager (enabling, disabling, command info), and general performance optimizations.  
Version: 1.15.2  

### Modded Server JARS

- [Forge](http://files.minecraftforge.net/) - Forge is a server software based on the MCP. Both the server and client need to be running the mods.  
Version: 1.1 - 1.16.5  

- [Fabric](https://fabricmc.net/) - Fabric, unlike Forge, is not based on the MCP. This allows it to be updated for snapshots easier. **It is incompatible with Forge.**  
Version: 1.14 - 21w06a (1.17 Snapshot)  

### Plugins and Mods

- [Magma](https://magmafoundation.org/) - Minecraft Forge hybrid server implementing the Spigot/Bukkit API (Cauldron for 1.12).  
Version: 1.12.2  

- [Mohist](https://mohistmc.com/) - Minecraft Forge hybrid server implementing the Paper/Spigot/Bukkit API(1.12.2/1.16). Formerly known as Thermos/Kettle/Cauldron/MCPC+.  
Version: 1.7.10, 1.12.2, 1.16.5  

- [Arclight](https://github.com/IzzelAliz/Arclight) - A Minecraft Bukkit(1.15/1.16) server implementation on Forge using Mixin.  
Version: 1.14 - 1.16  

- [SpongeForge](https://www.spongepowered.org/downloads/spongeforge) - SpongeForge allows both SpongeVanila plugins as well as Forge mods on one server.  
Version: 1.10.2 - 1.12.2  

- [Cardboard](https://www.curseforge.com/minecraft/mc-mods/cardboard) - Cardboard (formerly Bukkit4Fabric) is a Fabric mod that adds support for the popular Bukkit/Spigot modding API. This mod lets you use plugins that are made for Bukkit and it's derivatives (Spigot and Paper) with Fabric. It's not server software but allows Fabric servers to run Bukkit plugins.  
Version: 1.16.4 - 1.16.5  

- [AtomMC](https://github.com/josephworks/AtomMC) - Atom is a Minecraft Server Software that is based on Minecraft Forge and CraftBukkit for 1.12.2 version of Minecraft.  
Version: 1.12.2  

- MCPC+ - The First Hybrid server for Bukkit and Forge Combination.  

- KCauldron - A Fork of MCPC+ using Spigot instead of CraftBukkit.  

- Thermos - A Fork of KCauldron with many bug fixes and performance improvements.  

- Contigo - A fork of Thermos that was opened after Thermos was discontinued and allowed the community to add patches and bug fixes.  

- Uranium - A fork of KCauldron that added new features and bug fixes and is a very popular server choice in China.  

- CatServer - A Server designed for Forge and Paper support not based on any other preexisting software.  

- Kettle - A fork of Contigo that was updated to 1.12.2 and later 1.14.4 which adds support Paper and Forge Support.  
Version: 1.12.2 - 1.14.4  

- TableCloth - A Hybrid jar forked from AtomMC combining Forge + Spigot and a couple of Paper Patches.  

## Network Software

- [BungeeCord](https://www.spigotmc.org/wiki/bungeecord/) - Base for the Waterfall fork, these JARs are used for configuring networks of which an example is Hypixel or Mineplex, it is used for distributing workload and players to different lobbies (Different server instances run with separate files and data).
No, this can't be used as a normal JAR and requires at least 3 servers/instances, one is BungeeCord (or it's fork) which is called the proxy, players connect to this proxy and are sent to the default server which is set in config. Let's say server "Lobby" is the default, it will send you there, then you can connect to another server, for example, "Survival" which is running in a separate server/instance and BungeeCord enables the functionality travel across these different servers without returning to the multiplayer menu screen. (It can be done with special plugins which utilize BungeeCord API to send you to the chosen server on click, you'll most commonly see it as a compass or portal).  

- [Waterfall](https://papermc.io/downloads#Waterfall) - Fork of BungeeCord, faster than BungeeCord and has general improvements and tweaks which make it the more preferred network JAR, works the same as BungeeCord (talking about the use, it doesn't have a different system).  

- [Velocity](https://velocitypowered.com/) - A next-generation Minecraft proxy focused on scalability and flexibility. It allows server owners to link together multiple Minecraft servers so they may appear as one.  

- [Travertine](https://github.com/PaperMC/Travertine) - Fork of Waterfall with added `1.7.10` support if you want that old school experience.  

- [FlameCord](https://github.com/2LStudios-MC/FlameCord) - FlameCord is a patch for Travertine to fix possible exploits and add useful functionalities.  

- [HexaCord](https://github.com/CronixMC/HexaCord) - A fork of BungeeCord that added forge support before Waterfall did.  

- [LilyPad](http://www.lilypadmc.org/) - A separate Proxy with its API and Plugins that has been suggestively discontinued.  

- Aegis - A fork of BungeeCord that adds many security features and authentication features.  

- [Gate](https://github.com/minekube/gate) - A Minecraft Proxy that is written in Go suggesting "scalability, flexibility & excellent server version support".  

- [XCord](https://www.mc-market.org/resources/16843/) - A 1.7-1.16.x BungeeCord fork with built in anti-bot, anti-exploit, and many performance optimizations.  
Version: 1.7.10 - 1.16.5  