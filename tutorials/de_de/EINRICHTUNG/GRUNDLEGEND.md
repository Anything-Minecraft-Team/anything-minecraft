# Intro

Hier wird dir gezeigt, wie du lokal auf deinem Computer einen Minecraft Server hosten kannst (Muss aber nicht lokal sein, es gibt auch Anleitungen für Server).

## Einrichtung

Bevor man irgendetwas tut, sollte man sich sicher sein, alle Voraussetzungen zu haben. Es wird eine aktuelle Java-Version benötigt, zur Zeit ist das die Version 15.0.2, der Download ist bei `https://www.oracle.com/java/technologies/javase-jdk15-downloads.html`

Die Voraussetzungen für die Hardware sind nicht besonders hoch, aber beschränken den Server-Typ. Wenn du nur einen Vanilla-Server mit ein paar Spielern haben willst, dann ist das nicht sehr wichtig, aber wenn du mehr darüber lernen willst. Viele CPU-Kerne bringen nur wenig, da Minecraft nur in einem Thread ("in einem Kern") läuft, sondern man sollte sich eher darauf konzentrieren, dass ein Thread viel Leistung bringt. Zudem braucht man auch ein bisschen RAM, 2-4 GB für Vanilla-Server aber eher 8 GB für Server mit Plugins und/oder Mods.

Wenn du alle Voraussetzungen hast, musst du das passende Server-JAR finden (siehe [Das richtige Server-JAR finden](Das_richtige_Server_JAR_finden.md))
Wenn du nur einen Vanilla-Server haben willst, ist es sinnvoll, die JARs von [MCVersions](https://mcversions.net) herunterzuladen, da dort auch ältere Versionen verfügbar sind.

### Einrichtung auf Windows

Nachdem du das Server-JAR heruntergeladen hast, erstelle einen neuen Ordner und kopiere das JAR in diesen Ordner und benenne es zu `server.jar`. Jetzt brauchen wir noch eine Datei, um den Server auch auszuführen, also erstelle eine Datei namens `run.bat` und schreibe das folgende in diese Datei:

```sh
java -Xmx1024M -Xms1024M -jar server.jar nogui
PAUSE
```

![Das Server-JAR und die `run.bat`-Datei](https://i.imgur.com/RDvuoer.png)

Das `1024M` steht, dafür, dass der Server 1024 MiB, also 1 GiB RAM bekommt. 1024 oder 2048 sollten erst einmal reichen, bei Mods oder Plugins muss man vielleicht noch mehr zuteilen. Jetzt können wir den Server ausführen, also doppelklicke die Datei `run.bat`. Dadurch öffnet sich ein neues Konsolenfenster. Dort wird nach kurzer Zeit der Text `You need to agree to the EULA in order to run the server. Go to eula.txt for more info.` auftauchen. Bearbeite die neu generierte Datei `eula.txt` und ersetze `eula=false` mit `eula=true`. Dann doppelklicke nochmal `run.bat` Jetzt kannst du dein Minecraft starten und dich mit dem Server verbinden. Dafür schreibe als Server-Adresse `localhost` oder `127.0.0.1`.


### Einrichtung auf Linux

Achtung: Du solltest eher den Package Manager (zum Beispiel `apt(-get)` auf Ubuntu und Debian) benutzen um Java installieren

Erstelle einen Ordner, zum Beispiel `~/server`

--> `mkdir ~/server`

Kopiere dein Server-JAR in diesen Ordner und benenne es um zu `server.jar`

--> `mv ~/Downloads/spigot-1.16.5.jar ~/server/server.jar`

Erstelle eine Datei namens `start.sh` und schreibe in diese: `java -Xmx1024M -jar server-jar nogui` (es kann sein, dass das `nogui` nicht benötigt wird)

--> `echo "java -Xmx1024M -jar server.jar nogui" > start.sh`

Jetzt füge Ausführungs-Berechtigungen dem Skript zu und führe es aus

--> `chmod +x start.sh`

--> `./start.sh`

Jetzt wird nach kurzer Zeit der Text `You need to agree to the EULA in order to run the server. Go to eula.txt for more info.` auftauchen, also musst du die neue Datei `eula.txt` bearbeiten und das `eula=false` mit `eula=true` ersetzen

--> `echo "eula=true" > eula.txt` (Achtung: Dies überschreibt den Kommentar mit dem Link zur EULA)

Jetzt führe den Server (bzw das `start.sh`) erneut aus. Jetzt kannst du dein Minecraft starten und dich mit dem Server verbinden. Dafür schreibe als Server-Adresse `localhost` oder `127.0.0.1`.

#### Einrichtung für Server

Man braucht einen "service", wenn der Server z. B. automatisch starten oder neustarten soll.
Erstelle eine Datei namens `minecraft.service` in `/etc/systemd/system` (es kann sein, dass man root-Berechtigungen braucht)

--> `sudo touch /etc/systemd/system/minecraft.service`

Und dann fülle die Datei mit folgendem:

```txt
[Unit]
Description=A Minecraft Server
After=network.target
StartLimitIntervalSec=0[Service]
Type=simple
Restart=always
RestartSec=1
User={DEINBENUTZERNAME}
ExecStart=/home/{DEINBENUTZERNAME}/server/start.sh
```

ersetze `{DEINBENUTZERNAME}` mit deinem Benutzernamen

--> `sudo echo "[Unit]\nDescription=A Minecraft Server\nAfter=network.target\nStartLimitIntervalSec=0[Service]\nType=simple\nRestart=alwaysRestartSec=1\nUser=$USER\nExecStart=$HOME/server/start.sh" > /etc/systemd/system/minecraft.service`

jetzt kannst du den Service starten

--> `systemctl start minecraft`

Jetzt solltest du dem Server beitreten können.
Der Server wird 1 Sekunde, nachdem er heruntergefahren ist, automatisch neustarten. Wenn der Server starten soll, wenn der Server startet, musst du es enablen

--> `systemctl enable minecraft`

#### Einrichtung für Docker

Um Docker zu benutzen, erstelle eine Datei namens `Dockerfile` und schreibe Folgendes in sie:

```dockerfile
FROM openjdk
WORKDIR /root

COPY ["server.jar","eula.txt", "start.sh"] ./

EXPOSE 25565

ENTRYPOINT ["/root/start.sh"]
```

--> `echo "FROM openjdk\nWORKDIR /root\nCOPY ["server.jar","eula.txt", "start.sh"] ./\nEXPOSE 25565\nENTRYPOINT ["/root/start.sh"]" > Dockerfile`

Jetzt kannst du das Docker-Image bauen

--> `docker build . -t mcserver` (Du kannst `mcserver` ersetzen durch was du willst (außer es gibt ein gleichnamiges Image auf DockerHub))

Jetzt kannst du einen Container starten

--> `docker run --name mcserver -p 25565:25565 -d --restart unless-stopped mcserver`


Oder du benutzt Docker-Compose, dann schreibe folgendes in eine Datei namens `docker-compose.yml`:

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

und starte es

--> `docker-compose up -d`
