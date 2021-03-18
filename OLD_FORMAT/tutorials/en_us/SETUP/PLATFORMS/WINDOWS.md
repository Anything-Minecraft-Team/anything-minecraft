# Setup For Windows

After downloading your server jar create a new folder. You can name it anything you want.

![Create folder](/IMAGES/BASIC/CREATE_FOLDER.png)

Once you've done that, drag the server jar into the folder and rename it `server` so we can access it easily in the next step. Next, we need to create the file to run the server jar, you will need to enable file extensions if you haven't already.

![Enable file extensions](/IMAGES/BASIC/ENABLE_FILE_EXTENSIONS.png)

Create a new text document and name it "run", now open it and type

```sh
java -Xmx1024M -Xms1024M -jar server.jar nogui
PAUSE
```

![Text file](/IMAGES/BASIC/TEXT_FILE.png)

1024M is how many megabytes of RAM is allocated to the server, 1024M or 2048M is good for our purpose. If you ever need to change the amount just change the values. Save the file and close your text editor, go to the file in File Explorer and right-click, rename, and highlight the file extension "txt" and type "bat".

![Batch file](/IMAGES/BASIC/BAT_FILE.png)

This changes it to a batch file so we can run the server jar. We are ready to run the server now! Double click the run.bat file and it should come up with a new terminal window and after a while say "Agree to the Minecraft EULA".

![Agree to eula](/IMAGES/BASIC/AGREE_TO_EULA.png)

Close out of the terminal window and find a file called `eula.txt` that was generated. Open it and change `eula=false` to `eula=true`, save it then double click `run.bat` again.

![EULA file](/IMAGES/BASIC/EULA_FILE.png)

It may take a while for all the files to generate so be patient, once it's done your server should be good to go!
To join the server open Minecraft, go to multiplayer and add a new server, in the server IP add "localhost", click done and join your very own Minecraft server!

![Add localhost](/IMAGES/BASIC/ADD_LOCALHOST.png)

If you would like to be able to access the server from outside your local network, you're going to have to do what's called Port Forwarding, essentially allowing traffic to flow in and out through your router through a specific port to the computer that you're running the server on. Keep in mind this varies from ISP to ISP and from router to router, so a good guide dependent on your router is [here](https://portforward.com/). By default you're going to want to port forward the port 25565 for both the TCP and UDP protocols. To check whether the port forward fully worked, we recommend heading over to this [website](https://www.yougetsignal.com/tools/open-ports/) while your minecraft server is open (preferably after a restart post port forwarding), plug in the port you'd like to check, and if it says open you're good! If not, there might be something you're going to have to redo along the process.

Another reason a port forward might have failed is the windows firewall. To configure this, navigate to the windows defender control panel screen, and head over into advanced settings (you will need admin to do this). Go into inbound rules and outbound rules, and create a new rule for each, name it whatever you like, and make sure that it is allowing the port 25565 on BOTH TCP and UDP (you might need to set up 2 rules for each side). Once that is done, windows should no longer block a server running on that port on your machine.

Note: some ISPs have built in security funcitons in the router itself (looking at you xFinity), and as such they may block people from connecting to the server. While we do not recommend turning off a security function for the everyday user, in some instances it is required.

This process is slightly different for a modded server so we will go over it here!
