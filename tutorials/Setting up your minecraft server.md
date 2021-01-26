### Intro
I will now show you how to run and join your minecraft server. This will all be done locally on your computer.

### Setup
This setup is for windows.
The first thing you want to do after downloading your server jar is to create a new folder, you can name it anything you want. Once you've done that, drag the server jar into the folder. Now rename it "server" so we can access it easily in the next step. 


Next we need to create the file to run the server jar, you will need to enable file extensions if you havent already. Create a new text document and name it "run", now open it is type "java -Xmx1024M -Xms1024M -jar server.jar nogui PAUSE". 1024M is how many megabytes are allocated to the server, 1024M or 2048M is good for our purpose. Save the file and close your text editor, go to the file in File Explorer and right click, rename, and highlight the file extension "txt" and type "bat". 

This changes it to a batch file so we can run the server jar. We are ready to run the server now! Double click the run.bat file and it should come up with a new terminal window and after a while say "Agree to the minecraft EULA". Close out of the terminal window and find a file called "eula.txt" that was generated. Open it and change "eula=false" to "eula=true", save it then double click run.bat again. 

It may take a while for all the files to generate so be patient, once it's done your server should be good to go!
To join the server open minecraft, go to multiplayer and add new server, in the server ip add "localhost", click done and join your very own minecraft server!

This process is slightly different for modded server so I will go over it here!
