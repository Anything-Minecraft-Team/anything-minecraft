# Changing server settings

In this tutorial i assume you use [PaperSpigot](https://papermc.io/downloads), we are discussing the following points and more:

- Changing the server appearance in the serverlist

- Setting maximum playercount

- More things (feel free to add something)

## Changing server appearance

Go to your server folder. Here will you find multiple files. First we are going to edit the **Server.properties** file. Search for `motd`, the default is `motd=A Minecraft Server`. Now we are going to change that to something a bit more personal and colorful. Change the part after `motd=` to someting that you like, to use colors you add a Minecraft motd color code (see graphic below), for example: `motd=\u00A76Anything Minecraft!` displays "Anything Minecraft!" in gold.
![motd color codes](https://lazerstudiozgaming.files.wordpress.com/2015/01/screen-shot-2015-01-03-at-11-27-44-am.png?)
You can also change the server icon, that's the icon left from the motd in the serverlist. For this you need a PNG image scaled dow to 64x64 pixels. Paste this in your server folder (the same where your Jar is located) and rename it to `server-icon.png`.

## Setting maximum playercount

For this part you need to find `max-players` in the **Server.properties**, simply change this to the amount of players you want on your server. For 10+ players it is recommended to have at least 4Gb RAM allocated.
