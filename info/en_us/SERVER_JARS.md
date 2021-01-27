# Intro

Here we will go into as much detail as possible about each server jar you can use for your server

## [Vanilla](https://getbukkit.org/download/vanilla)

Vanilla is the original server jar that is distributed by Mojang. Plugins and mods are not supported on this. Behaves exactly like normal singleplayer Minecraft.

## [CraftBukkit](https://getbukkit.org/download/craftbukkit)

CraftBukkit was the first server jar to support plugins. It is the least optimized server jar that has plugin support. It is currently being supported by SpigotMC.

## [SpigotMC](https://getbukkit.org/download/spigot)

Spigot is a fork of Bukkit, it has better performance and more features, it also allows you to connect servers with Bungeecord.

## [PaperMC](https://papermc.io/downloads)

PaperMC is another fork, but this time it’s a fork of Spigot, it aims to get better performance out of spigot which it does amazingly. It’s updated much more often than Spigot (up to several times a day). This way PaperMC fixes bugs and exploits way quicker then Spigot. Of all the forks, Paper is the most used for recent versions of Miencraft.
A selection of added features and optimalizations:

- Async chunck loading and saving
- Timings reports
- No-tick view distance
- Several optimisations on TNT, hoppers and restone

## [Tuinity](https://github.com/Spottedleaf/Tuinity)

Tuinity is a fork of PaperMC that adds better performance especially for servers with high playercounts.

## [Purpur](https://github.com/pl3xgaming/Purpur)

Purpur is also a fork of PaperMC but has all Tuinity's features. It is recommended to use this over the other forks, if you are interested in a server with unique features, as it’s the most feature rich. It also has flying squids which is it's best feature.
Some of the features it adds:

- Lots of tweaks for entities. For example: make all mobs ridable, change max health
- Change mechanics. Such as: mine spawners with sulk touch, mending repairs most damaged equipment, totems of undying are working when only in inventory
- Lots more

## [YatopiaMC](https://github.com/YatopiaMC/Yatopia)

YatopiaMC has a bunch of features that could help make your server run faster. Therefore it combining the optimizations of many forks and optimization mods.
It has had some bugs that break the game, it is not tested in extend and doesn’t have all of Purpur’s features. Only very few servers are using this fork. If you don’t need an feature exclusive for YatopiaMC, it’s better to go with one of the above forks.

## [Fabric](https://fabricmc.net/)

Fabric is a modloader like forge but much more lightweight. It’s growing in popularity. It also has some of the best fps improving mods for the client (See Sodium mod) and server.

## Proxies

Proxies are servers meant to connect multiple servers together, as a network. These servers can run on the same machine, but even on different machines on different locations. Running your server as a network, can greatly improve performance, as Minecraft can spread the load over multiple cores. But it’s also adding complexity, as setting up and managing multiple servers isn’t as simple as managing one server.

### [Bungeecord](https://ci.md-5.net/job/BungeeCord/)

### [Waterfall](https://papermc.io/downloads#Waterfall)

Waterfall is a fork of Bungeecord. It’s Paper’s version of Bungeecord. It’s aming for mare features an more scalability. In the same way as how Paper relates to Spigot, Waterfall relates to Bungeecord. It pushes much more updates then Bungeecord.
