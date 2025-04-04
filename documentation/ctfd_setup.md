## Setting up the CTFd framework

New server on hetzner, ubuntu 24.05 image, 4gb ram, amd shared 3cpu, possibility to upgrade later

![](assets/1742497778823.png)

![](assets/1742497790387.png)

connecting to vps:

![](assets/1742293308609.png)


### updating server

```
apt update && apt upgrade
```

### prerequisities

Just docker for now

```
apt install docker.io docker-compose
```

cloning the github into /opt/

```
git clone https://github.com/CTFd/CTFd.git
```

Setting up secret key in docker-compose.yml

### Theme

Choosing a theme from
https://github.com/CTFd/themes

https://github.com/hmrserver/CTFd-theme-pixo/

Trying this out to be a starter

cloning the theme into /opt/CTFd/CTFd/themes

starting up the docker

```
docker-compose up
```

### First startup

first startup on the webapp launches the setup

![](assets/1742498355925.png)

![](assets/1743155835172.png)

We chose user mode for our platform, (no teams)

![](assets/1743155845221.png)

![](assets/1743155860537.png)

![](assets/1742498429095.png)

