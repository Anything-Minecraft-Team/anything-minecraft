# Picking a Server JAR

## What is a Server JAR?

<!---- [a server jar is blah blah something] --->

Here we will go into as much detail as possible about each server jar you can use for your server

### What is a fork?

Later, we will use the term "fork" often. A fork is an extension on an original piece of open-source software, allowing for additional functionality and changes. The term "upstream" is used to describe the original software which a fork is based upon.

Software can also be a fork of multiple forks. For example, Tuinity is a fork of PaperSpigot which is a fork of Spigot which is a fork of CraftBukkit which is a fork of the original Minecraft Vanilla server software.

## Server JAR Options

### [Vanilla](https://www.minecraft.net/en-us/download/server)

Vanilla is the original server jar that is distributed by Mojang.
Plugins and mods are not supported on this.
Vanilla servers behaves like normal singleplayer Minecraft but with additional commands.
Minecraft has a simple config called `server.properties` which you can use to change some basic settings.
Some of the main settings are, `motd=A Minecraft Server`, this changes what is displayed under your server in the server list, `max-players=20`, this changes the max amount of players that can join the server at once, `view-distance=10`, this changes the max render distance you can set, on the client you can set it to a higher value but it wont display that far, and many more! To see the default config go [here](https://github.com/Anything-Minecraft-Team/anything-minecraft/blob/fork-info/resources/DEFAULT/server.properties).

Suggested versions: Any

For detailed information go [here](SERVER_JARS/VANILLA.md).

### [CraftBukkit](https://getbukkit.org/download/craftbukkit)

CraftBukkit was the first server jar to support plugins.
However, now it is the least optimized server JAR with plugin support.

It is currently being supported by SpigotMC after it shutdown in 2014 due to getting a DMCA takedown.
CraftBukkit is the closest you can get to vanilla Minecraft while being able to add plugins.

Do NOT use this for a public server if there are other options available.

CraftBukkit adds some more settings in a seperate config `bukkit.yml`. Some examples are the `spawn-limits` section that allows you to change the amount of entities that can spawn per world, `allow-end` which is very simple, is the End enabled?

Suggested versions: 1.0.0 - 1.4.5

For detailed information go [here](SERVER_JARS/CRAFTBUKKIT.md).

### [SpigotMC](https://getbukkit.org/download/spigot)

SpigotMC, or Spigot, is a fork of Bukkit with; better performance; more features; and allows you to connect servers with Bungeecord.
SpigotMC adds more config options in a new file called `spigot.yml` to help optimize and change how servers work. Must use this or a fork of SpigotMC for bungeecord to work.

Suggested versions: 1.4.6 - 1.7.10

### [PaperMC](https://papermc.io/downloads)

PaperMC, or PaperSpigot, is a fork of SpigotMC. It aims to provide better performance, being updated more often than Spigot.
With this, PaperMC is able to patch bugs and exploits faster than SpigotMC.
Paper is one of the most popular forks that helps with performance a ton.

Suggested versions: 1.8 - 1.12.2

<!---- REMOVED AS NOT BALANCED OPINION
A selection of added features and optimalizations:
-	Async chunck loading and saving
-	Timings reports
-	No-tick view distance
-	Several optimisations on TNT, hoppers and restone
--->

### [Tuinity](https://github.com/Spottedleaf/Tuinity)

Tuinity is a fork of PaperMC that is "aimed at imporiving server performance at high playercounts"

Suggested versions: 1.13.2 - Latest

<!---- MORE INFO NEEDED --->

### [Purpur](https://github.com/pl3xgaming/Purpur)

Purpur is a fork of Paper and Tuinity with the goal of providing new and interesting configuration options.

Suggested versions: 1.13.2 - Latest

<!----- REMOVED AS NOT BALANCED OPINION
Some of the features it adds:
-	Lots of tweaks for entities. For example: make all mobs ridable, change max health
-	Change mechanics. Such as: mine spawners with sulk touch, mending repairs most damaged equipment, totems of undying are working when only in inventory
-	Lots more
---->

### [YatopiaMC](https://github.com/YatopiaMC/Yatopia)

A fork of Tuinity, Yatopia combines & borrows code, aiming to allow your server to run faster.

Suggested versions: None

<!----- REMOVED AS NOT BALANCED OPINION

It has had some bugs that break the game, it is not tested in extend and doesn’t have all of Purpur’s features. Only very few servers are using this fork. If you don’t need an feature exclusive for YatopiaMC, it’s better to go with one of the above forks.
---->

### [Fabric](https://fabricmc.net/)

Fabric is a modloader, similar to Forge but much more lightweight.
Growing in popularity recently, it also has some of the best QOL client-side mods, but also new and improved server optimizing mods.

## Proxies

### What is a proxy?

Proxies are servers meant to connect multiple servers together, as a network. These servers can run on the same machine or even on different machines at different locations!
Running your server as a network can greatly improve performance, as Minecraft can spread the load over multiple cores.
However, it also adds complexity, as setting up and managing multiple servers isn’t as simple as managing one server.

### [BungeeCord](https://ci.md-5.net/job/BungeeCord/)

BungeeCord is the original Minecraft proxy which "acts as a proxy between the player's client and the connected Minecraft servers". This allows players to seamlessly be transferred between different servers.

### [Waterfall](https://papermc.io/downloads#Waterfall)

Waterfall is PaperMC's fork of BungeeCord. It aims to provide stability, scalibility and more features. Similar to PaperMC, it has more frequent updates than BungeeCord.

### [Velocity](https://velocitypowered.com/)

"Velocity is a next-generation Minecraft proxy focused on scalability and flexibility. It allows server owners to link together multiple Minecraft servers so they may appear as one." Pretty much a much more optimized alternative to BungeeCord and Waterfall, although lacks out-of-the-box support for most BungeeCord plugins.