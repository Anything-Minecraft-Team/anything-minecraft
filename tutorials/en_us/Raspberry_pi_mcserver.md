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
