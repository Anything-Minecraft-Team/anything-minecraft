Here you will learn how to ***easily*** make a minecraft server on a Raspberry Pi!

WARNING: You WILL have to open the port of your router, and i will not include a guide here because every router is different.

# Step 1
Open the terminal emulator and install git with this command: `sudo apt install git`. Then insert this: `git clone https://github.com/timof121/RasPiMC-Server.git`
Then put: `cd RasPiMC-Server/`

# Step 2
Now you need to install the server running the RasPiMC-install.sh, but before, you need to put: `chmod u+x RasPiMC-install.sh`
Now you can do: `./RasPiMC-install.sh` and it will start installing the server. When it asks you to install something, you just type "y" and just wait. By default it will build the latest spigot version (Currently 1.16.5). but if you want another version, you can download it from [GetBukkit](https://getbukkit.org/) and just rename it to spigot.jar!

# Step 3
Now that you have installed the server, you need to start the server with: `./start.sh`
If you want to change the max/min RAM, you can change it at the start.sh.

# Step 4
Now you can configure the server, play with your friends, download plugins...
You can find **a lot** of plugins on [SpigotMC](https://www.spigotmc.org/resources/) or [Bukkit](https://dev.bukkit.org/bukkit-plugins)
You may want to install plugins like WorldEdit or WorldGuard...
And this is the end of the tutorial.

# FAQ
Here are some basic answers.

## How to change RAM?
Open `start.sh` in nano (`nano start.sh`). You will see this:
`#!/bin/bash

java -Xms512M -Xmx1G -jar spigot.jar nogui`
java stands for summoning the java enviroment, -Xms512M means that the minium dedicated RAM is 512 MegaBytes, -Xmx1G means the same but this time that 1GB is the maxium amount. So if you want ti change RAM, just change the -Xmx argument.

## How do i get another Spigot version?
You have two ways; the first one is downloading form a mirror, and the second is building it yourself.
The first one is very simple: just go to any mirror like [GetBukkit](https://getbukkit.org/), click Downloads and select your version!
The second one is a bit more hard: first, run this command to create a folder called Buildtools `mkdir Buildtools`. Then run `cd Buildtools` to go to the folder that you created. Then run this in your terminal for downloading BuildTools `wget -O BuildTools.jar https://hub.spigotmc.org/jenkins/job/BuildTools/lastSuccessfulBuild/artifact/target/BuildTools.jar` and then run `java -jar BuildTools.jar --rev latest` to start building the latest Spigot JAR. You can change `latest` to almost any Minecraft version starting from 1.8. This may take more than 15 minutes if you are on a Pi 3 or lower. When the building process finishes, you will find both Spigot and Crafbukkit. Then just replace your server's `spigot.jar` with the new one.
