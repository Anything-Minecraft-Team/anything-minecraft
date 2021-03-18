# Setup For Docker

#### Prebuilt Docker

> Based on the docker image with the most pulls
> See [itzg/docker-minecraft-server for more details](https://github.com/itzg/docker-minecraft-server)

##### Simple Launch

```sh
docker run -d -p 25565:25565 --name mc -e EULA=TRUE itzg/minecraft-server
```

##### Docker Compose

```yml
version: "3"

services:
  mc:
    image: itzg/minecraft-server
    ports:
      - 25565:25565
    environment:
      EULA: "TRUE"
    volumes:
      # attach the relative directory 'data' to the container's /data path
      ./data:/data
```

#### You Build Docker

You can use an already built docker image or just create a Dockerfile with following content:

```dockerfile
FROM openjdk
WORKDIR /data

COPY ["server.jar","eula.txt", "start.sh"] ./

EXPOSE 25565

ENTRYPOINT ["/data/start.sh"]
```

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
    volumes: -./server:/root
```

and run it: `docker-compose up -d`
