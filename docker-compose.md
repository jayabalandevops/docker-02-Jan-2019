

# Docker Compose Installation

- Following the URL

Step 1. https://docs.docker.com/compose/install/

```shell
sudo curl -L "https://github.com/docker/compose/releases/download/1.25.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

```shell
sudo chmod +x /usr/local/bin/docker-compose
```

```shell
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

```shell
$ docker-compose --version
docker-compose version 1.25.0, build 1110ad01
```

# Hands on

Step 2. Docker images

```shell
docker run -d --rm --name quantum -p 18080:8080 spkane/quantum-game:latest
```

```shell
docker stop quantum
docker ps
```

```shell
cd ${HOME}
mkdir class-docker-images
$cd${HOME}/class-docker-images
git clone https://github.com/spkane/balance_game.git --config core.autocrlf=
cd balance_game
ls
cat Dockerfile
```

```shell
curl -s -S "https://registry.hub.docker.com/v2/repositories/library/alpine/tags/" | jq '."results"[]["name"]' | sort
```

```shell
cd ${HOME}/class-docker-images 
docker run --rm -d --name outyet-small -p 8090:18088 \     spkane/outyet:1.9.4-small 
docker export outyet-small -o export.tar 
tar -tvf export.tar 
docker stop outyet-small 
rm export.tar
```
