# Intro

I will now show you how to run and join your minecraft server. This will all be done locally on your computer.

## Setup

This setup is for windows.
The very first thing required in setting up a Minecraft server is to verify if you have all the prerequisites, be they software or hardware requirements. As for the software, an updated version of Java is highly recommended, and in some instances, required. These can be installed from oracle's website, and try to keep up on updating these as previously mentioned, it is sometimes required to have the latest version of Java (at the time of writing, the version is 15.0.2, for that version visit <https://www.oracle.com/java/technologies/javase-jdk15-downloads.html>).

As for the hardware requirements, they are not too strict, but they restrict what type of server you'll be running. If you don't particularly care for the performance of the server with a couple of players on a vanilla server, you should be fine to skip over this section, but if you're a hardware nerd or would like to learn more on the subject, this will attempt to enlighten you. When choosing parts for a Minecraft server, one should stray away from the higher-core-count CPUs and choose something with better single-threaded performance, as that is nearly all that Minecraft will use. Memory is often one of the most popularly sought after specs in a Server box, however a good computer alone it does not make. When choosing the parts for the computer, put more effort into finding a better CPU with the amount of RAM not as an afterthought, but a second priority. For all the servers I've run, I've found that using no more than 8GB per server works perfectly fine if in a modded environment, around 2-4GB for a vanilla/lightly-modded environment. Typically speaking, more memory allows for more players and more mods, but always make sure that your CPU is keeping up with the server itself before trying to throw more memory at the server, as sometimes with more memory comes worse performance due to how java is written.

Once you've figured through the prerequisites, you need to find the best server jar for your requirements; along with this thread there is a part for choosing a server jar, but if you'd rather go the easy route and stick with vanilla, a popular and quite useful to get the server jars from is <https://mcversions.net/>, as that contains legacy files along with newly released versions.

Now what you want to do after downloading your server jar is to create a new folder, you can name it anything you want. Once you've done that, drag the server jar into the folder. Now rename it "server" so we can access it easily in the next step. Next we need to create the file to run the server jar, you will need to enable file extensions if you havent already. Create a new text document and name it "run", now open it and type

```sh
java -Xmx1024M -Xms1024M -jar server.jar nogui
PAUSE
```

![server jar and run file](https://i.imgur.com/RDvuoer.png)

1024M is how many megabytes are allocated to the server, 1024M or 2048M is good for our purpose. Save the file and close your text editor, go to the file in File Explorer and right click, rename, and highlight the file extension "txt" and type "bat". This changes it to a batch file so we can run the server jar. We are ready to run the server now! Double click the run.bat file and it should come up with a new terminal window and after a while say "Agree to the minecraft EULA". close out of the terminal window and find a file called "eula.txt" that was generated. Open it and change "eula=false" to "eula=true", save it then double click run.bat again. It may take a while for all the files to generate so be patient, once it's done your server should be good to go!
To join the server open minecraft, go to multiplayer and add new server, in the server ip add "localhost", click done and join your very own minecraft server!

This process is slightly different for modded server so I will go over it here!
