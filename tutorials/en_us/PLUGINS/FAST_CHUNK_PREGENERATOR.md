# How to install and use [Fast Chunk Pregenerator](https://www.spigotmc.org/resources/fast-chunk-pregenerator.74429/)

## What is Fast Chunk Pregenerator?

Fast chunk pregenerator, or FCP, is a plugin that generates chunks of your world so it doesn't have to generate new chunks while people are exploring. It helps with server lag because generating new chunks takes up a lot of server resources. 

## Prerequisites

You need a server running which can handle Spigot plugins (for example Spigot, Paper or Purpur; look [here](../../../info/en_us/SERVER_JARS.md) for a further description of the servers)

The first thing to do is to download FCP. Go to [the Spigot Page](https://www.spigotmc.org/resources/fast-chunk-pregenerator.74429/) and click on `Download Now`

[![Image of the Spigot Page](../../../resources/PLUGINS/FAWE/FAWE_SPIGOT.png)](https://www.spigotmc.org/resources/fast-async-worldedit.13932/)

## Installation

Move (or copy) the downloaded JAR into the plugins directory in your server directory (where the Server JAR is)

Now restart your server (do `/restart` or do `/stop` and start it again).

Note: You can also do `/reload` but that is not recommended and can cause bugs and memory leaks.

## Using FCP

### Getting Started

Before we start, never use this plugin while people are playing on your server, it causes extreme lag. Don't worry, the lag is normal as it's generating lots of chunks.

To use these commands you either need access to the console, have operator or have the `fcp.commands` permission.

To get started go to the server console and type `/fcp start <radius> [world] [chunkX] [chunkZ]`. 
- `radius` is how many blocks outwards you want to be generated. 
- `world` is what world you want to be generated, works with custom worlds with multiverse and similar plugins. 
- `chunkX` is the X coordinate you want the generation to start on. 
- `chunkZ` is the Y coordinate you want the generation to start on.

Once you have run the command it will start generating the chunks, all you have to do now is wait.

### Pause, Resume and Cancel Generation Tasks

FCP has some useful commands that allow you to pause, resume and cancel generation tasks. 

#### Pausing Generation

To pause a generation task run the command `/fcp pause`

#### Resuming Generation

To resume a generation task after pausing it, run the command `/fcp resume`

#### Canceling Generation

To cancel a generation task run the command `/fcp cancel`

### Pending Generation Tasks

You can have a queue of generation tasks by running the command in [Getting Started](FAST_CHUNK_PREGENERATOR.md#getting_started) multiple times. 

To view the pending generation task run the command `/fcp pending`