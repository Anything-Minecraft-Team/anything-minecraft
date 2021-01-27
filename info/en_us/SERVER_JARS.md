# Picking a Server JAR

## What is a Server JAR?

[a server jar is blah blah something]

Here we will go into as much detail as possible about each server jar you can use for your server

### What is a fork?

Later, we will use the term "fork" often. A fork is a <><>


## Server JAR Options

### [Vanilla](https://www.minecraft.net/en-us/download/server)

Vanilla is the original server jar that is distributed by Mojang. 
Plugins and mods are not supported on this. 
Vanilla servers behaves like normal Singleplayer Minecraft.

### [CraftBukkit](https://getbukkit.org/download/craftbukkit)

CraftBukkit was the first server jar to support plugins. 
However, now it is the least optimized server JAR with plugin support. 
It is currently being supported by SpigotMC.

### [SpigotMC](https://getbukkit.org/download/spigot)

SpigotMC, or Spigot, is a fork of Bukkit with; better performance; more features; and allows you to connect servers with Bungeecord.

### [PaperMC](https://papermc.io/downloads)

PaperMC, or PaperSpigot, is a fork of SpigotMC. It aims to provide better performance, being updated more often than Spigot. 
With this, PaperMC is able to patch bugs and exploits faster than SpigotMC. 
<!---- REMOVED AS NOT BALANCED OPINION
A selection of added features and optimalizations:
-	Async chunck loading and saving
-	Timings reports
-	No-tick view distance
-	Several optimisations on TNT, hoppers and restone 
--->

### [Tuinity](https://github.com/Spottedleaf/Tuinity)

Tuinity is a fork of PaperMC that is "aimed at imporiving server performance at high playercounts"
<!---- MORE INFO NEEDED --->

### [Purpur](https://github.com/pl3xgaming/Purpur)

"Purpur is a fork of Paper and Tuinity with the goal of providing new and interesting configuration options.

<!----- REMOVED AS NOT BALANCED OPINION
Some of the features it adds:
-	Lots of tweaks for entities. For example: make all mobs ridable, change max health
-	Change mechanics. Such as: mine spawners with sulk touch, mending repairs most damaged equipment, totems of undying are working when only in inventory
-	Lots more
---->

### [YatopiaMC](https://github.com/YatopiaMC/Yatopia)

A fork of Tuinity, Yatopia combines & borrows code, aiming to allow your server to run faster.

<!----- REMOVED AS NOT BALANCED OPINION

It has had some bugs that break the game, it is not tested in extend and doesn’t have all of Purpur’s features. Only very few servers are using this fork. If you don’t need an feature exclusive for YatopiaMC, it’s better to go with one of the above forks.
---->

### [Fabric](https://fabricmc.net/)

Fabric is a modloader, similar to Forge but much more lightweight. 
Growing in popularity recently, it also has some of the best QOL client-side mods, but also new and improved server optimizing mods.


## Proxies

Proxies are servers meant to connect multiple servers together, as a network. These servers can run on the same machine or even on different machines at different locations! 
Running your server as a network can greatly improve performance, as Minecraft can spread the load over multiple cores. 
However, it also adds complexity, as setting up and managing multiple servers isn’t as simple as managing one server.

### [BungeeCord](https://ci.md-5.net/job/BungeeCord/)

### [Waterfall](https://papermc.io/downloads#Waterfall)

Waterfall is a PaperMC's fork of BungeeCord. It aims to provide stability, scalibility and more features. Similar to PaperMC, it has more frequent updates than BungeeCord.


