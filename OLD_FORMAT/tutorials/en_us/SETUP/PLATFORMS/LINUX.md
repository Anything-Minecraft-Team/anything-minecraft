# Setup For Linux

> Warning: You should prefer using your package manager (for example `apt` on Ubuntu and Debian) to install java because it's more organized with the package manager

You can do this using the following command

--> `sudo apt install openjdk-xx-jre`

`xx` being the version number you're aiming for. (You can view available versions using `sudo apt-cache search openjdk`)

Create a folder, for example named "server", for example in your home directory (`~`)

--> `mkdir ~/server`

Copy your server jar to this folder and rename it to "server.jar"

--> `mv ~/Downloads/spigot-1.16.5.jar ~/server/server.jar` (supposing your server jar is in `~/Downloads` and it's name is `spigot-1.16.5.jar`)

Create a text document named `start.sh` and write into it:
`java -Xmx1024M -jar server-jar nogui` (the `nogui` might not be required)

--> `echo "java -Xmx1024M -jar server.jar nogui" > start.sh`

now add execute permissions to the script and run it

--> `chmod +x start.sh`

--> `./start.sh`

This will say something like
`You need to agree to the EULA in order to run the server. Go to eula.txt for more info.`
so you have to edit `eula.txt` to say `eula=true` instead of `eula=false`

--> `echo "eula=true" > eula.txt` (Warning: This overwrites the comment with the link to the EULA)

now launch the server / execute `start.sh` again

--> `./start.sh`

You have your server running. To join, launch Minecraft and join the server at `127.0.0.1` or `localhost`

If you want to start the server and want to be able to exit out of the terminal without the server closing, there are two ways with which you can do this

- You can use an in-built linux utility called [tmux](https://github.com/tmux/tmux/wiki). Use this if the server is intended to be temporarily up.
- You can register minecraft as a **system service**. Use this if the server is intended to be up 24/7 and requires automatic restarting in case of host shutdowns/failures.

#### Setup With Tmux

Start a tmux window

`tmux new-session -t sessionName`

`sessionName` being whatever you want to name the instance, for example `minecraft-session`

This will automatically take you inside the tmux session. Start the server using

`java -Xmx1024M -Xms1024M -jar server-jar nogui`

Exit out of the tmux session using `Ctrl+B` **then** `D`

You server will keep running in the background.

To reattach to the session,

`tmux a -t sessionName`

`sessionName` being whatever you named the instance earlier.

To destroy the session completely, you can attach to the session and then `Ctrl+D` out of it. It detaches from session and destroys it too.

#### Setup As A System Service

You need to set up a service if it should, for example automatically launch at boot or restart when it terminates
So, create a file named `minecraft.service` in `/etc/systemd/system` (May require root permissions)

--> `sudo touch /etc/systemd/system/minecraft.service` (actually optional)

And write into it:

```txt
[Unit]
Description=A Minecraft Server
After=network.target
StartLimitIntervalSec=0[Service]
Type=simple
Restart=always
RestartSec=1
User={YOURUSERNAME}
ExecStart=/home/{YOURUSERNAME}/server/start.sh
```

of course, replace `{YOURUSERNAME}` with your username

--> `sudo echo "[Unit]\nDescription=A Minecraft Server\nAfter=network.target\nStartLimitIntervalSec=0[Service]\nType=simple\nRestart=alwaysRestartSec=1\nUser=$USER\nExecStart=$HOME/server/start.sh" > /etc/systemd/system/minecraft.service`
so you can now start the service

--> `systemctl start minecraft`

Now you should be able to join
It will restart automatically 1 second after it shut down. To make it start at boot, enable it

--> `systemctl enable minecraft`
