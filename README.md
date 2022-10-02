## 👋 Welcome to whoogle 🚀  

whoogle README  
  
  
## Run container

```shell
dockermgr update whoogle
```

### via command line

```shell
docker pull casjaysdevdocker/whoogle:latest && \
docker run -d \
--restart always \
--name casjaysdevdocker-whoogle \
--hostname casjaysdev-whoogle \
-e TZ=${TIMEZONE:-America/New_York} \
-v $HOME/.local/share/srv/docker/whoogle/files/data:/data:z \
-v $HOME/.local/share/srv/docker/whoogle/files/config:/config:z \
-p 80:80 \
casjaysdevdocker/whoogle:latest
```

### via docker-compose

```yaml
version: "2"
services:
  whoogle:
    image: casjaysdevdocker/whoogle
    container_name: whoogle
    environment:
      - TZ=America/New_York
      - HOSTNAME=casjaysdev-whoogle
    volumes:
      - $HOME/.local/share/srv/docker/whoogle/files/data:/data:z
      - $HOME/.local/share/srv/docker/whoogle/files/config:/config:z
    ports:
      - 80:80
    restart: always
```

## Authors  

🤖 casjay: [Github](https://github.com/casjay) [Docker](https://hub.docker.com/r/casjay) 🤖  
⛵ CasjaysDevDocker: [Github](https://github.com/casjaysdevdocker) [Docker](https://hub.docker.com/r/casjaysdevdocker) ⛵  
