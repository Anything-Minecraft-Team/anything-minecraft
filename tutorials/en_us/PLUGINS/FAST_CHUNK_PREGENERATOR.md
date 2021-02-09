# How to install and use [Fast Chunk Pregenerator](https://www.spigotmc.org/resources/fast-chunk-pregenerator.74429/)

## What is Fast Chunk Pregenerator?

Fast Chunk Pregenerator, or FCP, is a plugin that generates chunks of your world so it doesn't have to generate new chunks while people are exploring. It helps with server lag because generating new chunks takes up a lot of server resources. 

## Prerequisites

You need a server running which can handle Spigot plugins (for example Spigot, Paper or Purpur; look [here](../../../info/en_us/SERVER_JARS.md) for a further description of the servers)

Now what you need to do is download FCP. Go to [the Spigot Page](https://www.spigotmc.org/resources/fast-chunk-pregenerator.74429/) and click on `Download Now`

[![Image of the Spigot Page](../../../IMAGES/PLUGINS/FAST_CHUNK_PREGENERATOR/DOWNLOAD_EXAMPLE.PNG)](https://www.spigotmc.org/resources/fast-chunk-pregenerator.74429/)

## Installation

Move (or copy) the downloaded JAR into the plugins directory in your server directory (where the Server JAR is).

Now restart your server (do `/restart` or do `/stop` and start it again).


## Using FCP

### Getting Started

Note: Never use this plugin while people are playing on your server, it causes extreme lag. Don't worry, the lag is normal as it's generating lots of chunks.

To use these commands you either need access to the console, have operator or have the `fcp.commands` permission.

To get started go to the server console and type `/fcp start <radius> [world] [chunkX] [chunkZ]`. 
- `radius` is how many blocks outwards you want to be generated. 
- `world` is what world you want to be generated, works with custom worlds with multiverse and similar plugins. 
- `chunkX` is the X coordinate you want the generation to start on. 
- `chunkZ` is the Z coordinate you want the generation to start on.

Once you have run the command it will start generating the chunks, all you have to do now is wait. It may take a long time if you are generating thousands of blocks outwards.

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
