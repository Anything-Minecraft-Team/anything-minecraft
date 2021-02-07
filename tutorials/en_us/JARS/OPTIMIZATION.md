# Introduction

Here you will learn how to optimize you Minecraft server to get better performance.

## Optimizing your .jar specific configurations to YOUR NEEDS

Every .jar has its own set of configurations that you can tweak to suit your specific needs. You probably wont find as effective the config of a minigames server in a survival server. You should read every config, understand it, and choose if you need to use it or not. This is extremely important in survival servers as some config values can ruin your mob spawning rates or destroy your players custom redstone circuits.

Here is a [guide](https://www.spigotmc.org/threads/guide-server-optimization⚡.283181/) made by a well-known member of the community that can help you further in this optimization, it is limited to PaperMC and doesn't have optimized configs for Tuinity, Purpur or any other forks. You can also join [this discord](https://discord.gg/yev2rN3eZH), which has an amazing Discord bot that assists you optimizing your server based on your timings report! Remember this is a general suggestion, it may not suit your needs.

Another essential step in survival servers is to pre-generate your world, because chunk generation consumes a lot of resources. One of several possible ways is shown below

1. Download and install [Fast Chunk Pregenerator](https://www.spigotmc.org/resources/fast-chunk-pregenerator.74429/)
2. Set your desired world limit.
3. Use the command: `/fcp start <radius> [world] [chunkX] [chunkZ]`
4. Wait for it to finish, it may take a long time and the server will lag while it works. This **MUST** be done with the server empty / closed to public.

For a guide on Fast Chunk Pregenerator go [here](../../../tutorials/en_us/PLUGINS/FAST_CHUNK_PREGENERATOR.md).

## Aikars Flags / Startup Flags

You should also use correct startup flags, the [Aikars flags](https://aikar.co/2018/07/02/tuning-the-jvm-g1gc-garbage-collector-flags-for-minecraft/)!
Sadly many server hosts won't allow you to use these. An exeption is [Birdflop Hosting](https://www.birdflop.com/).