# Advanced JAR picking

If you want to go a little more in-depth with JAR picking, you've come to the right place.

## Server Software

Server software is the software that allows multiple players to play on a server together.

### Note

A * means that the developer of that project mass produces them. This leads to a lack of support, lack of updates, and quick abandonement.

### Plugins:

- [CraftBukkit](https://getbukkit.org/download/craftbukkit) - It's the BASE for all forks that are out today and they still are updating it to this day, not newbie friendly at all because it requires manual building (or you can get it [here](https://getbukkit.org)). The only real use is for Minecraft versions from `1.0.0` to `1.4.5` as there is no Spigot release for these versions.  
Version: 1.0.0 - 1.16.5  
Currently Active

- [SpigotMC](https://www.spigotmc.org/) - The original fork of Bukkit. Spigot has improved performance vs CraftBukkit, still widely used. It's a recommended alternative if for some reason you don't want to use PaperMC.  
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

- [FoxSpigot](https://www.mc-market.org/resources/8592/)* - FoxSpigot is a fork of Spigot aiming to make PvP servers perform better.  
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

- [SharpMC](https://github.com/SharpMC/SharpMC) - A 1.8 server made from scratch in C#.  
Version: 1.8.x  
DISCONTINUED

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

- [DytanicSpigot](https://cloudnetservice.eu/repositories/de/dytanic/dytanicspigot-api/) - Other than its API it has been lost to time, but it was a Spigot fork said to be capable of stability hitting 40 TPS, although there's not much left of it to show if it was.  
Version: ???  
DISCONTINUED

- [xSpigot](https://www.mc-market.org/resources/11411/) - A 1.7.10 - 1.8.x TacoSpigot fork with custom knockback editing and options such as toggleable mob AI. This is meant for HCF servers and practice PvP servers.  
Version: 1.7.10 - 1.8.x  
DISCONTINUED

- [ySpigot](https://www.mc-market.org/resources/7198/) - ySpigot is a remake of xSpigot for later versions of Minecraft.  
Version: 1.7.10 - 1.12.x
DISCONTINUED

- zSpigot - A 1.7.10 Paper fork with huge optimizations, completely custom knockback editing, built-in server benchmarking, and more PvP based features. Ironically, despite it originally being a premium resource the only way to get it now is through a leaks website due to the creator leaking resources.  
Version: 1.7.10  
DISCONTINUED

- [mSpigot](https://www.mc-market.org/resources/6864/)* - Another premium TacoSpigot fork with promises of improved TNT and knockback aimed at PvP and Factions servers.  
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

- [TorchSpigot](https://github.com/TorchSpigot/Torch) - The now abandoned predecessor to Akarin based on a goal of getting Paper to run on multiple threads.  
Version: ???  
DISCONTINUED

- [APOLLO16 ](https://www.mc-market.org/resources/16271/) - A 1.16.5 Purpur fork with a built-in system monitor and optimized block and chunk ticking methods.  
Version: 1.16.5  
Currently Active

- [LightSpigot 1.8.8](https://www.mc-market.org/resources/16933/) - A free 1.8.8 Spigot fork focused on adding some optimizations and features for HCF servers, like enderpearls teleporting through slabs.  
Version: 1.8.8  
Currently Active

- [LightSpigot 1.16.5](https://www.mc-market.org/resources/17753/) - A 1.16.5 Spigot fork with some spawner / general performance optimizations and custom knockback editing.  
Version: 1.16.5  
Currently Active

- [VoltaneSpigot](https://www.mc-market.org/threads/571429/) - A 1.8.8 based TacoSpigot fork with built-in 1.7 - 1.16 client support with multi-thread support, custom knockback editing, discord server integration, and a lot of factions based features.  
Version: 1.8.8  
DISCONTINUED

- [SSSpigot](https://www.mc-market.org/resources/14122/) - A 1.16.5 Paper fork with multi-thread support, useless code removal, some general optimizations, and tracking metrics disabled.  
Version: 1.16.5  
Currently Active

- [RocketMC](https://www.mc-market.org/resources/13898/) - A 1.15.2 Tuinity fork with a built-in monitoring system, plugin manager (enabling, disabling, command info), and general performance optimizations.  
Version: 1.15.2  
DISCONTINUED

- [aSpigot](https://www.mc-market.org/resources/6101/)* - aSpigot is a premium 1.7.10 Paper fork with custom knockback editing, togglable features like mob AI, and various features pointed at HCF servers.  
Version: 1.7.10  
Currently Active

- [BeeSpigot](https://www.mc-market.org/resources/14263/)* - BeeSpigot is a premium 1.15.2 Paper fork with custom knockback editing, togglable features like mob AI, and some general optimizations.  
Version: 1.15.2  
Currently Active

- [CoronaSpigot](https://www.mc-market.org/resources/14170/)* - CoronaSpigot is a premium 1.8.8 Paper fork with custom knockback editing and some general optimizations.  
Version: 1.8.8  
Currently Active

- [Fish](https://github.com/CraftLight-Network/Fish) - Fish is a 1.16.5 Purpur fork with features that are too niche to be added to Purpur.  
Version: 1.16.5  
Currently Active

- [GuardSpigot](https://www.mc-market.org/resources/14497/) - GuardSpigot is a 1.8.8 $99 premium TacoSpigot fork with features like custom knockback editing, lag machine detection, and a bunch of features you can toggle like mob AI for performance gain/gameplay change.  
Version: 1.8.8  
Currently Active

- [NachoSpigot](https://github.com/CobbleSword/NachoSpigot) - NachoSpigot is a 1.8.8 TacoSpigot fork aimed at bringing modern patches and optimizations to 1.8.  
Version: 1.8.8  
DISCONTINUED

- [Rainforest](https://github.com/Proximyst/Rainforest) - RainForest is a 1.16.1 - 1.16.5 Paper fork with optimizations that they're testing out/optimizations that they plan to keep to themselves.  
Version: 1.16.1 - 1.16.5  
Currently Active

- [SportBukkit](https://github.com/StratusNetwork/SportBukkit) - SportBukkit is a fork of CraftBukkit improving stability and adding some new features. It was developed for and by the StratusNetwork server.  
Version: 1.8 - 1.12.2  
DISCONTINUED

- [SportPaper](https://github.com/StratusNetwork/SportPaper) - SportPaper is a 1.8.8 fork of Paper improving performance even more. It is developed for and by the StratusNetwork server.  
Version: 1.8  
DISCONTINUED

- [SternalSpigot](https://www.mc-market.org/resources/18663/)* - SternalSpigot is a premium 1.8.8 TacoSpigot fork that tries to move a lot of processes to an async system, has some general optimizations, and has some knockback profiles to switch between for different results.  
Version: 1.8.8  
Currently Active

- [wSpigot](https://www.mc-market.org/resources/6874/)* - wSpigot is a 1.7.10 Paper fork with custom knockback profiles, built-in 1.8 client support, and a lot of HCF based features/optimizations.  
Version: 1.7.10  
Currently Active

- [CanaryMod](https://github.com/CanaryModTeam/CanaryMod) - A fork of hMod for implementing some of Bukkit's patches. Used on the MinecraftOnline server.  
Version: ???  
DISCONTINUED

- [Cauldron-js](https://github.com/vantezzen/cauldron-js) - Cauldron-js is just a proof of concept idea of running a 1.13.2 server entirely inside your web browser. Doesn't run great, but still an achievement.  
Version: 1.13.2  
DISCONTINUED

- [Feather](https://github.com/feather-rs/feather) - Feather is a recode of Minecraft servers entirely in the Rust programming language, aimed at making the server run multicore - this would significantly increase performance. It currently only supports 1.16.5. Worth noting, their plugin API is not finished yet either.  
Version: 1.16.5  
Currently Active

- [hMod](https://github.com/traitor/Minecraft-Server-Mod/) - The first server type with server-side mods (plugins) supported. It supported early Alpha versions.  
Version: ???  
DISCONTINUED

- [NeptuneVanilla](https://github.com/NeptunePowered/NeptuneMod) - A continuation of CanaryMod under a new repository and name.  
Version: 1.8.9 - 1.9  
DISCONTINUED

- [Project-Rainbow](https://ci.codecrafter47.de/job/Rainbow/) - Project-Rainbow was an attempt at overthrowing Bukkit with a new platform, but as we can tell that didn't work.  
Version: 1.13.2  
DISCONTINUED

- [PaperBin](https://github.com/x4e/PaperBin) - PaperBin is a fork of paper, it patches dupes, bugs and more. It aims to continue 1.12.2 paper and provide support. You can even use it on top of custom paper forks because it uses JVMTI to modify Minecraft classes at runtime.  
Version: 1.12.2  
Currently Active

### Modded Server JARS

- [Forge](http://files.minecraftforge.net/) - Forge is server software based on the MCP. Both the server and client need to be running the same mods.  
Version: 1.1 - 1.16.5  
Currently Active

- [Fabric](https://fabricmc.net/) - Fabric, unlike Forge, is not based on the MCP. This allows it to be updated for snapshots easier. **It is incompatible with Forge.**  
Version: 1.14 - 21w06a (1.17 Snapshot)  
Currently Active

- [ModLoaderMP](https://mcarchive.net/mods/modloadermp) - ModLoaderMP was the first multiplayer mod loader, supporting from Beta 1.4 to release 1.5.2.  
Version: Beta 1.4 - 1.5.2

### Plugins and Mods

- [Magma](https://magmafoundation.org/) - Minecraft Forge hybrid server implementing the Spigot/Bukkit API (Cauldron for 1.12).  
Version: 1.12.2  
Currently Active

- [Mohist](https://mohistmc.com/) - Minecraft Forge hybrid server implementing the Paper/Spigot/Bukkit API(1.12.2/1.16). Formerly known as Thermos/Kettle/Cauldron/MCPC+.  
Version: 1.7.10, 1.12.2, 1.16.5  
Currently Active

- [Arclight](https://github.com/IzzelAliz/Arclight) - A Minecraft Bukkit(1.15/1.16) server implementation on Forge using Mixin.  
Version: 1.14 - 1.16  
Currently Active

- [SpongeForge](https://www.spongepowered.org/downloads/spongeforge) - SpongeForge allows both SpongeVanila plugins as well as Forge mods on one server.  
Version: 1.10.2 - 1.12.2  
Currently Active

- [Cardboard](https://www.curseforge.com/minecraft/mc-mods/cardboard) - Cardboard (formerly Bukkit4Fabric) is a Fabric mod that adds support for the popular Bukkit/Spigot modding API. This mod lets you use plugins that are made for Bukkit and it's derivatives (Spigot and Paper) with Fabric. It's not server software but allows Fabric servers to run Bukkit plugins.  
Version: 1.16.4 - 1.16.5  
Currently Active

- [AtomMC](https://github.com/josephworks/AtomMC) - Atom is a Minecraft Server Software that is based on Minecraft Forge and CraftBukkit for 1.12.2 version of Minecraft.  
Version: 1.12.2  
Currently Active

- [Hotpur](https://github.com/ishlandbukkit/Hotpur) - HotPur is a 1.16.5 fork of Purpur attempting to add Fabric mod support.  
Version: 1.16.4  
Currently Active

- [MCPC+](https://ci.md-5.net/job/Cauldron/) - MCPC+ was a 1.2.5 to 1.7.10 Bukkit/Forge hybrid, the first of its kind. It was also known as Cauldron. 

- [KCauldron](https://github.com/djoveryde/KCauldron) - KCauldron is a fork of MCPC+ using Spigot instead of CraftBukkit.  
Version: 1.7.10  
DISCONTINUED

- [Thermos](https://github.com/CyberdyneCC/Thermos) - A Fork of KCauldron with many bug fixes and performance improvements.  
Version: 1.7.10  
DISCONTINUED

- [Contigo](https://github.com/djoveryde/Contigo) - A fork of Thermos that was opened after Thermos was discontinued and allowed the community to add patches and bug fixes.  
Version: ???  
DISCONTINUED

- [Uranium](https://github.com/UraniumMC/Uranium) - A fork of KCauldron that added new features and bug fixes and is a very popular server choice in China.  
Version: ???  
DISCONTINUED

- [CatServer](https://github.com/Luohuayu/CatServer) - A Server designed for Forge and Paper support not based on any other preexisting software.  
Version: 1.12.2  
Currently Active

- [Kettle](https://github.com/KettleFoundation/Kettle) - A fork of Contigo that was updated to 1.12.2 and later 1.14.4 which adds support Paper and Forge Support.  
Version: 1.12.2 - 1.14.4  
Currently Active

- TableCloth - A Hybrid jar forked from AtomMC combining Forge + Spigot and a couple of Paper Patches.  
Version: ???  
DISCONTINUED

- [Lava](https://github.com/Timardo/Lava) - Lava is a 1.12.2 Forge/Spigot hybrid server not forked from any other hybrid servers.  
Version: 1.12.2  
DISCONTINUED

- [NeptuneForge](https://github.com/NeptunePowered/NeptuneForge) - A hybrid of Forge/NeptureVanilla. NeptuneVanilla being the fork of CanaryMod.  
Version: ???  
DISCONTINUED

- [PFServer](https://github.com/l89669/PFServer) - PFServer is a 1.12.2 fork of AtomMC and CatServer to create a better Forge/Bukkit hybrid.  
Version: ???  
DISCONTINUED

## Network Software

- [BungeeCord](https://www.spigotmc.org/wiki/bungeecord/) - Base for the Waterfall fork, these JARs are used for configuring networks of which an example is Hypixel or Mineplex, it is used for distributing workload and players to different lobbies (Different server instances run with separate files and data).  
No, this can't be used as a normal JAR and requires at least 3 servers/instances, one is BungeeCord (or it's fork) which is called the proxy, players connect to this proxy and are sent to the default server which is set in config. Let's say server "Lobby" is the default, it will send you there, then you can connect to another server, for example, "Survival" which is running in a separate server/instance and BungeeCord enables the functionality travel across these different servers without returning to the multiplayer menu screen. (It can be done with special plugins which utilize BungeeCord API to send you to the chosen server on click, you'll most commonly see it as a compass or portal).  
Version: 1.8 - 1.16.5  
Currently Active

- [Waterfall](https://papermc.io/downloads#Waterfall) - Fork of BungeeCord, faster than BungeeCord and has general improvements and tweaks which make it the more preferred network JAR, works the same as BungeeCord (talking about the use, it doesn't have a different system).  
Version: 1.8 - 1.16.5  
Currently Active

- [Velocity](https://velocitypowered.com/) - A next-generation Minecraft proxy focused on scalability and flexibility. It allows server owners to link together multiple Minecraft servers so they may appear as one.  
Version: 1.7.2 - 1.16.5  
Currently Active

- [Travertine](https://github.com/PaperMC/Travertine) - Fork of Waterfall with added `1.7.10` support if you want that old school experience.  
Version: 1.7 - 1.16.5  
Currently Active

- [FlameCord](https://github.com/2LStudios-MC/FlameCord) - FlameCord is a patch for Travertine to fix possible exploits and add useful functionalities.  
Version: 1.7 - 1.16.5
Currently Active

- [HexaCord](https://github.com/CronixMC/HexaCord) - A fork of BungeeCord that added forge support before Waterfall did.  
Version: 1.7 - 1.11  
DISCONTINUED

- [LilyPad](http://www.lilypadmc.org/) - A separate Proxy with its API and Plugins that has been suggestively discontinued.  
Version: ???  
Currently Active

- [Aegis](https://polymart.org/resource/31) - A fork of BungeeCord adding many security measures and with built-in anti-bot and anti-VPN. It supports 1.7.x to 1.16.3. The developer is currently falsely banned from MC-Market.  
Version: 1.7 - 1.16.4  
DISCONTINUED

- [Gate](https://github.com/minekube/gate) - A Minecraft Proxy that is written in Go suggesting "scalability, flexibility & excellent server version support".  
Version: ???  
Currently Active

- [XCord](https://www.mc-market.org/resources/16843/) - A 1.7-1.16.x BungeeCord fork with built in anti-bot, anti-exploit, and many performance optimizations.  
Version: 1.7.10 - 1.16.5  
Currently Active

- [BarelyAuthenticated](https://github.com/Mindgamesnl/BarelyAuthenticated) - A fork of BungeeCord which caches players IPs and usernames to verify them while Mojang services are unstable. It is created and maintained for the server BlockParty.  
Version: 1.8 - 1.16  
Currently Active

- [DarkCord](https://github.com/Oculate/DarkCord) - A fork of HexaCord/BungeeCord used and made by the Oculate Network.  
Version: 1.7.x - 1.11.x  
DISCONTINUED

- [DasBungee](https://www.mc-market.org/resources/17481/) - DasBungee is a premium BungeeCord fork that adds an IP blacklist system and patches "all known exploits".  
Version: 1.8 - 1.16.5  
Currently Active

- [Flexagon](https://github.com/SeaEclipse/Flexagon) - Flexagon is a fork of Hexacord and Travertine meant just for testing purposes.  
Version: 1.7 - 1.15.2  
DISCONTINUED

- [Glymur](https://github.com/StratusNetwork/Glymur) - Glymur is a fork of Travertine adding in some bug fixes and Stratus APIs. It is developed by the StratusNetwork server.  
Version: 1.7 - 1.14  
DISCONTINUED

- [GoLilyPad](https://github.com/LilyPad/GoLilyPad) - A rewrite of Lilypad in the programming language Go.  
Version: ???  
Currently Active

- [Gravity](https://www.mc-market.org/resources/17731/) - Gravity is a premium BungeeCord fork adding features like antibot, global messaging, and patches for almost all of the issues.  
Version: ???  
Currently Active

- [GuardHexa](https://www.mc-market.org/resources/16180/) - GuardHexa is a premium fork of HexaCord that patches a lot of bugs/exploits and has a bit of optimization.  
Version: 1.7 - 1.16.4  
Currently Active

- [HQBungeeCord](https://github.com/moyugame/HQBungeeCord) - HQBungeeCord is a Waterfall fork aimed at improving stability and performance.  
Version: ???  
DISCONTINUED

- [InsaneProxy](https://www.mc-market.org/resources/16588/) - InsaneProxy is a premium fork of Travertine and Velocity, resulting in lower CPU usage and more exploits patched.  
Version: 1.7 - 1.16.5  
Currently Active

- [Miners-League-BungeeCord](https://github.com/root1599/Miners-League-BungeeCord) - MLBC is a fork of BungeeCord created by and used by the Miners League Minigames Network for any custom patches/features they may need.  
Version: ??? - 1.13  
DISCONTINUED

- [NachoBungee](https://github.com/CobbleSword/NachoBungee) - NachoBungee is by the guys from NachoSpigot, which is a bad sign. On the GitHub page, they list off features of what they forked, nothing new.  
Version: 1.7 - 1.16  
Currently Active

- [SecureCord](https://www.mc-market.org/resources/15002/) - SecureCord is a free BungeeCord fork which patches from harmful exploits.  
Version: ???  
DISCONTINUED

- [SSCord](https://www.mc-market.org/resources/14562/) - SSCord is a premium fork of Waterfall adding some optimizations, anti-bot features like captcha, and patches some waterfall exploits.  
Version: 1.7.2 - 1.16.5  
Currently Active

- [VanillaCord](https://github.com/ME1312/VanillaCord/tree/1.12) - VanillaCord is a BungeeCord fork allowing Vanilla servers to connect through BungeeCord.  
Version: 1.12 - 1.16.5  
Currently Active

- [WaterCrash](https://www.mc-market.org/resources/13579/) - WaterCrash is a premium WaterFall fork adding 1.7.x support, adds real-time IP blacklisting, and a crash/exploit preventer. Currently, the resource purchase page is deleted for unknown reasons.  
Version: 1.7 - 1.15  
DISCONTINUED

- [wCord](https://github.com/wtfaremyinitials/wCord) - A fork of BungeeCord with animated MOTDs.  
Version: 1.4.7 - 1.6.4  
DISCONTINUED

- [zBungeeCord](https://www.mc-market.org/resources/10187/) - zBungeeCord is a premium BungeeCord fork optimizing BungeeCord quite a bit and cleaning up the commands.  
Version: 1.7 - 1.8  
DISCONTINUED
