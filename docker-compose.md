

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

