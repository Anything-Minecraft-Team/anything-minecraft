# Introduction

Here you will learn how to optimize you Minecraft server to get better performance.

## Different kinds of Lag

TPS - Server Lag
**TPS** stands for **T**icks **P**er **S**econd. It is also the only lag type a server owner has direct control over.

A server processes all tasks at a rate of 20 TPS. Tasks like mob movement, crop growth, and player interactions with blocks need to be ticked by the server to function properly. A TPS below 20 means the server is running behind and must skip tasks in order to keep important tasks on time. Significant TPS loss usually presents itself with minor annoyances like intermittent mob freezing and block break resets. Severe cases could result in server-wide freezes or even crashes.

**TPS Ratings**
- 20.0 = Flawless - Well done.
- 19.95-19.99 = Great - Unnoticeable TPS loss. Most servers live here.
- 18.5-19.94 = Fair - Maybe some annoyances, but nothing game-ruining.
- 16.0-18.4 = Poor - You definitely need to fix it if this is your average.
- <16.0 = Unplayable...


**Ping - Connection Lag**
**Ping** (aka latency) reflects how long (in milliseconds) data takes to process and travel between the client and server host. The further a client is geographically separated from the server, the longer this transfer might take. Other common influences on ping are congested or slow connections.

As a server owner (assuming you have a choice) you should host your server in a region where you prefer to have your player base or one that appeases a broad range of players.

**Ping Ratings**
- 1-90 = Great!
- 91-179 = Good - Maybe a slight disadvantage in PvP.
- 180-299 = Poor - Regular lag while interacting with blocks/players/entities.
- 300-499 = Bad - Nearly unplayable.
- 500+ = Assuming your bandwidth is solid, it's time to find a server closer to you.


**FPS - Client Lag**
Do not confuse TPS with **FPS** (**F**rames **P**er **S**econd). FPS reflects a client's ability to process and display what the game/server wants to render. FPS is 100% client side and has nothing to do with server performance.

The only thing a server can do to help FPS is cut server features so dinosaur PCs can keep up, but even that is unlikely to make a big difference. Instead of reducing server features, recommend a popular client mod called Optifine to players.

**FPS Ratings**
Note: These rates assume your standing average in a non-graphic-intense location.

- 60+ = Perfect - Anything over 60 FPS is overkill for Minecraft. Consider capping FPS below 80 to avoid unnecessary stress on hardware.
- 40-59 = Great - Should have no issues.
- 25-39 = Good - Occasional rendering lag. Issues if you enter graphic-intense areas.
- 15-24 = Poor - Constant rendering glitches. Probably freeze in GI area.
- 1-10 = Bad - Client should significantly reduce graphic settings.

## What's lagging? - measuring performance

### mspt
Paper offers a /mspt command that will tell you how much time server took to calculate recent ticks. If the first and second value you see are lower than 50, then congratulations! Your server is not lagging! If the third value is over 50 then it means there was at least 1 tick that took longer. That's completely normal and happens from time to time, so don't panic.

### timings
Great way to see what might be going on when your server is lagging are timings. Timings is a tool that lets you see exactly what tasks are taking the longest. It's the most basic troubleshooting tool and if you ask for help regarding lag you will most likely be asked for your timings.

To get timings of your server you just need to execute /timings paste command and click the link you're provided with. You can share this link with other people to let them help you. It's also easy to misread if you don't know what you're doing. There is a [detailed video tutorial by Aikar](https://www.youtube.com/watch?v=T4J0A9l7bfQ) on how to read them.

### spark
[Spark](https://github.com/lucko/spark) is a plugin that allows you to profile your servers CPU and memory usage. You can read on how to use it on its [wiki](https://github.com/lucko/spark/wiki/Commands). There's also a guide on how to find the cause of lag spikes [here](https://github.com/lucko/spark/wiki/Finding-the-cause-of-lag-spikes).

## Optimizing your .jar specific configurations to YOUR NEEDS

Every .jar has its own set of configurations that you can tweak to suit your specific needs. You probably wont find as effective the config of a minigames server in a survival server. You should read every config, understand it, and choose if you need to use it or not. This is extremely important in survival servers as some config values can ruin your mob spawning rates or destroy your players custom redstone circuits.

Here is a [guide](www.spigotmc.org/threads/guide-server-optimization⚡.283181/page-1) made by a well-known member of the community that can help you further in this optimization, it is limited to PaperMC and doesn't have optimized configs for Tuinity, Purpur or any other forks. You can also join [this discord](https://discord.gg/yev2rN3eZH), which has an amazing Discord bot that assists you optimizing your server based on your timings report! Remember this is a general suggestion, it may not suit your needs.

## Aikars Flags / Startup Flags

You should also use correct startup flags, the [Aikars flags](https://aikar.co/2018/07/02/tuning-the-jvm-g1gc-garbage-collector-flags-for-minecraft/)!
Sadly many server hosts won't allow you to edit startup flags by yourselft, but they are likely to do it for you if you open a ticket.

## World Pre-Generation

Another essential step in survival servers is to pre-generate your world, because chunk generation consumes a lot of resources. One of several possible ways is shown below

1. Download and install [Fast Chunk Pregenerator](https://www.spigotmc.org/resources/fast-chunk-pregenerator.74429/)
2. Set your desired world limit.
3. Use the command: `/fcp start <radius> [world] [chunkX] [chunkZ]`
4. Wait for it to finish, it may take a long time and the server will lag while it works. This **MUST** be done with the server empty / closed to public.

For a guide on Fast Chunk Pregenerator go [here](../../../tutorials/en_us/PLUGINS/FAST_CHUNK_PREGENERATOR.md).

## "Too good to be true" plugins

### Plugins removing ground items
Absolutely unnecessary since they can be replaced with merge radius and alt-item-despawn-rate and frankly, they're less configurable than basic server configs. They tend to use more resources scanning and removing items than not removing the items at all.

### Mob stacker plugins
It's really hard to justify using one. Stacking naturally spawned entities causes more lag than not stacking them at all due to the server constantly trying to spawn more mobs. The only "acceptable" use case is for spawners on servers with a large amount of spawners.

### Plugins enabling/disabling other plugins
Anything that enables or disables plugins on runtime is extremely dangerous. Loading a plugin like that can cause fatal errors with tracking data and disabling a plugin can lead to errors due to removing dependency. The /reload command suffers from exact same issues.