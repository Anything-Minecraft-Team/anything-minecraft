# Remote Server Management

The goal of this tutorial is to give you everything you need to manage your server when you don't have access to the physical machine. This tutorial is primarily for someone on a Windows system connecting to a Linux	server.

---

### Table of Contents

[Command Line Access (SSH)](#command-line-access-ssh)
 - [PuTTY](#putty)
	 - [Shortcut Setup](#shortcut-setup)

[tmux](#tmux)
 - [Attaching Sessions](#attaching-sessions)
 - [Sending keys](#sending-keys)
 - [Shortcuts](#shortcuts)

[File Management (FileZilla)](#file-management-filezilla)
 - [Connecting](#connecting)
 - [Navigation](#navigation)
 - [Transferring Files](#transferring-files)
 - [Editing Files](#editing-files)

[Conclusion](#conclusion)

---

## Command Line Access (SSH)

Since a lot of interaction with a Minecraft server is through its command line terminal, your primary tool for interacting with your remote server will be SSH.

[SSH (Secure Shell)](https://en.wikipedia.org/wiki/SSH_(Secure_Shell)) is a tool that allows you to securely connect to a remote computer. You can use it through any terminal; below is me using SSH in the default Windows CMD to connect to a server on my local network.

![](https://i.imgur.com/xXKWJCK.png)

The basic syntax for this is `ssh <username>@<IP address>`. It'll prompt you for a password, and then you're in.

However, there are better tools for using SSH, like PuTTY.

### PuTTY

[PuTTY](https://www.chiark.greenend.org.uk/~sgtatham/putty/) is a very well-regarded free SSH program. Here's a view of the main menu below:

![](https://i.imgur.com/wxQE3ec.png)

Don't worry, though—you don't have to learn any of that. One of the best parts of PuTTY is that you can bypass having to enter your credentials, letting PuTTY take care of that for you. This is done through a shortcut with arguments.

#### Shortcut Setup

1. Find the default PuTTY shortcuts.

	 - Press the Windows key <kbd>Win</kbd> and search for "putty". Right-click on the app result, and click "Open file location".
	 
	 - The default location for this is `C:\ProgramData\Microsoft\Windows\Start Menu\Programs\PuTTY (64-bit)`.

2. Copy the "PuTTY" shortcut, and paste it in the directory `C:\Users\<username>\AppData\Roaming\Microsoft\Windows\Start Menu\Programs`. You can rename it to something recognizable by you, such as "SSH Minecraft Server".

3. Open the shortcut's properties (Right-click, "Properties").

4. In "Target", enter this: `"C:\Program Files\PuTTY\putty.exe" -ssh <username>@<IP address> -pw <password>`. Be sure to add your proper credentials. You may need to change your path to `putty.exe` if you have it installed in a different location.

	 - This gives PuTTY arguments to use when you start it. The arguments are the IP address/user you want to connect to, and the password to use for that user.
	 
	 - Note that this stores your password in plaintext. If you don't want that, you can remove the `-pw <password>` argument, and it will prompt you to enter your password each time you run the shortcut.

That's it! You now have a shortcut for PuTTY set up. You can open the shortcut by pressing the Windows key <kbd>Win</kbd> and searching for its name—this makes it super easy to open. You can use this SSH connection to do anything on the command-line that you'd be able to do with physical keyboard, mouse, and monitor access.

### tmux

tmux is an invaluable tool for a Linux server that allows you to have several processes running on different virtual windows, allowing you to switch between them. To explain better:

1. You SSH into your server. By default, you're now in the Linux terminal. 

2. You can run a tmux command that switches you to your Minecrft server's virtual window. Here, you can interact with your Minecraft server's terminal as normal.

3. You use a keyboard shortcut to switch back to the main Linux terminal. From here, you can interact with the Linux OS like normal. You can switch to other tmux virtual windows/processes, too, if you have other things going on.

If tmux isn't installed already, you can do so with this command: `sudo apt-get install tmux`.

You can use bash files and tmux commands to set up scripts to do all kinds of stuff to your server, but we'll go over some basic functionality now. [Here's a nice low-level tmux tutorial that goes into more detail.](https://www.howtogeek.com/671422/how-to-use-tmux-on-linux-and-why-its-better-than-screen/)

First, you need to create a tmux virtual window, called a session. Use the `cd` command to switch to your Minecraft server directory. Then, run the command `tmux new-session -d -s <session name>`. This starts a new tmux session in your current location. The `-d` starts the session detached, meaning you don't automatically switch to it. `-s <session name>` specifies the session's name, which is used to refer to it in other commands.

Now, there are a few things you can do to access the session.

#### Attaching sessions

##### Attaching

The tmux command for attaching a session is `tmux attach-session -t <session name>`. When you run it, your terminal will switch from the normal Linux terminal to the tmux session's terminal. While the session is attached, any commands run will be sent to that session.

For example, if you attach the session `tmux attach-session -t minecraft-server`, you can run the command `say Hello!`, and it will be sent to the Minecraft server command-line (saying "Hello!" as the server), not to the Linux command-line.

##### Detaching

To detach the tmux session, returning to the regular Linux terminal, use the keyboard shortcut <kbd>Ctrl</kbd> + <kbd>B</kbd>, then press <kbd>D</kbd>.

#### Sending keys

To send commands to the session without switching to it, use the command `tmux send-keys -t <session name>.0 "<command>" ENTER`. There's a lot to unpack in that command:

 - You're using the tmux command `send-keys` to send, well, key press input to a tmux session.
 
 - You're using `-t <session name>.0` to specify what tmux session you're referring to. The `-t` argument is used in tmux commands to do this. The `.0` at the end of the session name specifies the window you want to send the keys to. This tutorial doesn't use tmux windows, but they're pretty simple: you can have multiple windows in one tmux session, switching between them.
 
 - `"<command>" ENTER` has the actual keys you want sent to the tmux session. A single-line command is stored in the quotation marks, and by sending the key `ENTER` at the end you'll cause the session to actually run the command. You should be able to repeat this syntax several times to send multiple commands, or you can run the entire `tmux send-keys` command several times with a different command contained each time.
 
Here's an example of this:

```
tmux send-keys -t minecraft-server.0 "sh run_server.sh" ENTER
```

This sends the command `"sh run_server.sh" ENTER` to the tmux session `minecraft-server`. This will run the shell file `run_server.sh`, which probably starts the Minecraft server.

#### Shortcuts

Since tmux commands can get sort of long, I like to use Linux aliases to shorten them. These can be set up by editing the `.bashrc` file in your user's root directory.

In the `.bashrc` file, add this line to the end: `alias tmuxx="tmux attach-session -t $1"`. Save it and close it. Now, you can run the command `tmuxx <session name>`, and it will run the longer `tmux attach-session` command under the hood, attaching your session. The `$1` refers to the first argument after the `tmuxx` command.

## File Management (FileZilla)

You're going to need to be able to access the files on your Minecraft server's machine. This can be done through [SFTP (Secure File Transfer Protocol)](https://en.wikipedia.org/wiki/SSH_File_Transfer_Protocol).

The best way to use SFTP is with an SFTP client such as [FileZilla](https://filezilla-project.org/). You can see a picture of the FileZilla UI below:

![](https://i.imgur.com/JWWnShc.png)

### Connecting

After you've opened FileZilla, use the keyboard shortcut <kbd>Ctrl</kbd> + <kbd>S</kbd> to open the "Site Manager" menu, seen below:

![](https://i.imgur.com/CMhVtU0.png)

Here, you can specify the IP address and your credentials, very similar to SSH. After you've set it all up, click "Connect" to connect to the server using SFTP. You'll use <kbd>Ctrl</kbd> + <kbd>S</kbd> and "Connect" to connect to the server using SFTP from now on.

### Navigation

Now, you'll be able to view two locations:

 - Files in a local directory on your computer
 
 - Files in a remote directory on the remote server

You can navigate through each by entering a direct location in the text boxes above the directory viewers or by double-clicking on a directory (double-click `..` to go up one directory).

### Transferring Files

There are several methods for transferring files using FileZilla:

 - Select and drag files from one side to the other to transfer all of the selected files.
 
 - Double-click a file to transfer that single file. Note this behavior on a double-click; double-clicking doesn't run a file or open it in an editor.
 
### Editing Files

You can edit a file by right-clicking and selecting "View/Edit". To set a default file editor, open the settings ("Edit" --> "Settings" in the top-left) and set it up like I have below:

![](https://i.imgur.com/LhlpfRH.png)

Once you've finished editing the file, save it in your editor, and go back to FileZilla. You should be greeted with this prompt:

![](https://i.imgur.com/CA6U84E.png)

By selecting "Yes", the edited file will be transferred to the remote server, overwriting the existing file with your changes.

If "Finished editing and delete local file" isn't checked, you can continute to edit/save/revert changes on the local file in your editor. If you never check that box, when you close FileZilla it'll warn you that you still have a file locally:

![](https://i.imgur.com/bqw2uCb.png)

If you've finished everything you want to do, you can safely close FileZilla and the SFTP connection will be closed.

## Conclusion

Hopefully, these three tools (PuTTY, tmux, FileZilla) will give you what you need to remotely manage a Minecraft server. You can use them in lots of different ways. For example, here's one of my bash scripts, `start_hub.sh`, copied directly from my remote host:

```
#!/bin/sh

read -p 'Start or stop hub: ' Input
if [ "$Input" = "start" ]; then
	cd _Versions/hub
	tmux new-session -d -s hub
	tmux send-keys -t hub.0 "sh run_server.sh" ENTER
elif [ "$Input" = "stop" ]; then
	tmux send-keys -t hub.0 "stop" ENTER
	sleep 3s
	tmux kill-session -t hub
else
	tmux send-keys -t hub.0 $Input ENTER
fi 
```

Going into detail on this is outside the scope of this tutorial; however, hopefully this gives you a glimpse of the powerful abilities of these tools. Start small, and soon you'll have your host machine set up just the way you want. Good luck!