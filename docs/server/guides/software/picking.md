# Choosing a server software

Here we will go through how to pick the right server software for your server. Server software contains all the code for the server, there are some for modloaders, like [Forge](https://files.minecraftforge.net/net/minecraftforge/forge) or [Fabric](https://fabricmc.net/), and some that allow you to use plugins, like [Sponge](https://www.spongepowered.org) or [SpigotMC](https://www.spigotmc.org).

[Here](../../info/lists/server_software) is a list with lots of server software in one place.

## Picking your server software

The first step to deciding what server software you want to use is picking what type of server you want to run. If you already know, great! If not you should go and decide before reading further.

Now you need to think about what features your server needs, like chests, combat, redstone etc. If your server doesn't need many vanilla features you may want to look into using a server software built from the ground up, like [Minestom](https://minestom.net) or [Krypton](https://kryptonmc.org). The vanilla server will work for whatever you decide but will not have the performance compared to software without all the features.

### Vanilla Software

If you need the vanilla software's features, trying to decide between a server software for a vanilla server is hard, there are many forks claiming to be the best. If you don't need any plugins on your server you can use a [Fabric](https://fabricmc.net) server with server-side optimization mods. The most commonly used vanilla software with plugin support is [SpigotMC](https://www.spigotmc.org) and its forks, [PaperMC](https://papermc.io), [Purpur](https://purpur.pl3x.net) etc. Another popular vanilla software with plugin support is [SpongeVanilla](https://www.spongepowered.org/downloads/spongevanilla), its primary use is in forge-spigot hybrid servers, in the form of [SpongeForge](https://www.spongepowered.org/downloads/spongeforge), but it can be used with just vanilla. The [SpongeAPI](https://www.spongepowered.org/downloads/spongeapi) doesn't have as big of a variety of plugins created for it as [SpigotMC](https://www.spigotmc.org) so you might need to create some of the plugins yourself. There is server software that is designed/optimized for faction/KitPVP or some other types of gamemodes but many are mass-produced and are abandoned quickly.

### Custom Software

Custom software is created for better performance mainly targetting minigame servers. Some are trying to recreate the vanilla server with better performance and others are just an API and you need to recode every feature you want in the game. These are mostly good for minigame servers as the vanilla recodes are likely not finished.

### Modded Software

If you want to play with mods you will need a modded server software. There are a few of these but the most popular/still updated ones are [Fabric](https://fabricmc.net) and [Forge](https://files.minecraftforge.net/net/minecraftforge/forge). There are mod versions of plugins but not as much of a wide variety, hybrid servers (explained below) are better for this. [Fabric](https://fabricmc.net) is more commonly used for servers with mods that act as plugins.

### Hybrid Software

If you are running a hybrid server, mods and plugins, there are a few options. If you are looking for a hybrid server that supports Bukkit plugins it will be less stable than one that is built over the mod software as it mashes two different server software together and plugins may be incompatible with other mods. If you use one that is built around the modded software it will be more stable but likely will have a smaller variety of plugins available.

### Software to stay away from

It is a good idea to stay away from discontinued software and ones that support outdated versions but it's ultimately up to you. If you are deciding between a high-performance software that's not stable, like [YatopiaMC](https://yatopiamc.org) was, and one that has less performance but is much more stable it is generally a good idea to go with the one that is more stable. It is also a good idea to stay away from mass-produced server software, they mostly have copy-pasted code and it will quickly lead to a lack of support and abandonment.
