# Intro

I will now show you how to run and join your Minecraft server. This will all be done locally on your computer.

## Setup

The very first thing required in setting up a Minecraft server is to verify if you have all the prerequisites, be they software or hardware requirements. As for the software, an updated version of Java is highly recommended, and in some instances, required. These can be installed from oracle's website, and try to keep up on updating these as previously mentioned, it is sometimes required to have the latest version of Java (at the time of writing, the version is 15.0.2, for that version visit `https://www.oracle.com/java/technologies/javase-jdk15-downloads.html`).

As for the hardware requirements, they are not too strict, but they restrict what type of server you'll be running. If you don't particularly care for the performance of the server with a couple of players on a vanilla server, you should be fine to skip over this section, but if you're a hardware nerd or would like to learn more on the subject, this will attempt to enlighten you. When choosing parts for a Minecraft server, one should stray away from the higher-core-count CPUs and choose something with better single-threaded performance, as that is nearly all that Minecraft will use. Memory is often one of the most popularly sought after specs in a Server box, however a good computer alone it does not make. When choosing the parts for the computer, put more effort into finding a better CPU with the amount of RAM not as an afterthought, but a second priority. For all the servers I've run, I've found that using no more than 8GB per server works perfectly fine if in a modded environment, around 2-4GB for a vanilla/lightly-modded environment. Typically speaking, more memory allows for more players and more mods, but always make sure that your CPU is keeping up with the server itself before trying to throw more memory at the server, as sometimes with more memory comes worse performance due to how java is written.

Once you've figured through the prerequisites, you need to find the best server jar for your requirements; along with this thread there is a part for choosing a server jar, but if you'd rather go the easy route and stick with vanilla, a popular and quite useful to get the server jars from is <https://mcversions.net/>, as that contains legacy files along with newly released versions.

### Setup for Windows

Now what you want to do after downloading your server jar is to create a new folder, you can name it anything you want. Once you've done that, drag the server jar into the folder. Now rename it "server" so we can access it easily in the next step. Next, we need to create the file to run the server jar, you will need to enable file extensions if you haven't already. Create a new text document and name it "run", now open it and type

```sh
java -Xmx1024M -Xms1024M -jar server.jar nogui
PAUSE
```

![server jar and run file](https://i.imgur.com/RDvuoer.png)

1024M is how many megabytes are allocated to the server, 1024M or 2048M is good for our purpose. Save the file and close your text editor, go to the file in File Explorer and right-click, rename, and highlight the file extension "txt" and type "bat". This changes it to a batch file so we can run the server jar. We are ready to run the server now! Double click the run.bat file and it should come up with a new terminal window and after a while say "Agree to the Minecraft EULA". close out of the terminal window and find a file called "eula.txt" that was generated. Open it and change "eula=false" to "eula=true", save it then double click run.bat again. It may take a while for all the files to generate so be patient, once it's done your server should be good to go!
To join the server open Minecraft, go to multiplayer and add a new server, in the server IP add "localhost", click done and join your very own Minecraft server!

This process is slightly different for a modded server so I will go over it here!

### Setup for Linux

Warning: You should rather use your package manager (for example `apt` on Ubuntu and Debian) to install java because it's more organized with the package manager
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

#### Setup for servers

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

### Setup for docker

You can use an already built docker image or just create a Dockerfile with following content:

```dockerfile
FROM openjdk
WORKDIR /root

COPY ["server.jar","eula.txt", "start.sh"] ./

EXPOSE 25565

ENTRYPOINT ["/root/start.sh"]
```

--> `echo "FROM openjdk\nWORKDIR /root\nCOPY ["server.jar","eula.txt", "start.sh"] ./\nEXPOSE 25565\nENTRYPOINT ["/root/start.sh"]" > Dockerfile`
Now, supposing you have docker installed, build the docker image
--> `docker build . -t mcserver` (You can replace `mcserver`, the name of the image, with whatever you want (as long as it doesn't interfere with the images on dockerhub))
Run the docker image
--> `docker run --name mcserver -p 25565:25565 -d --restart unless-stopped mcserver`
or with docker compose, write following in a file named `docker-compose.yml`

```yml
version: "3"
services:
  mcserver:
    build: .
    restart: unless stopped
    ports:
      - 25565:25565
```

--> `echo "version: "3"\nservices:\n mcserver:\n build: .\n restart: unless stopped\n ports:\n - 25565:25565" > docker-compose.yml`
and run it
--> `docker-compose up -d`
