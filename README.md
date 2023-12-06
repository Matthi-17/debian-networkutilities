# debian-networkutilities
Debian build docker image with dnsutils, iputils-ping and iproute2

Hi :)

as part of my vocational training, I needed a container which supports ping, ip a, nslookup. At first I didn't want to build a container, then I thought I'd give it a try. And that's how this little container came into existence.

Included are:

debian:latest
dnsutils
iputils-ping
iproute2
ntp
with the latest updates. 

# How to start this container

normally a Docker Container is shutting down, in follow of this you need to add the tty flag

## Docker run:

```
docker run -ti matthi17/debian-networkutilities:latest

```

## Docker-Compose:

```
version: "3"

services:
  utilities:
    image: matthi17/debian-networkutilities:latest
    stdin_open: true 
    tty: true        

```

# How to use this container

will follow shortly

# How to build this image by your own:

## build with Dockerfile


1. downloaded the Dockerfile in a new directory

```
wget https://raw.githubusercontent.com/Matthi-17/debian-networkutilities/main/Dockerfile/Dockerfile

```

2. build your image

```
   docker build . -t matthi17/debian-networkutilities #use your image name

```

Upload to Docker Hub

docker push matthi17/debian-networkutilities:latest #use your repo name

# Links

[networkutilities on GitHub](https://github.com/Matthi-17/debian-networkutilities "Project on GitHub")

[networkutilities on Docker Hub](https://hub.docker.com/r/matthi17/debian-networkutilities "Project on Docker Hub")

[Offical Debian Image on Docker Hub](https://hub.docker.com/_/debian "Debian on Docker Hub")

