# debian-networkutilities
Debian build docker image with dnsutils, iputils-ping and iproute2

Hi :)

as part of my vocational training, I needed a container which supports ping, ip a, nslookup. At first I didn't want to build a container, then I thought I'd give it a try. And that's how this little container came into existence.

Included are:

debian:latest
dnsutils
iputils-ping
iproute2
with the latest updates. 


How to build this image by your own:

1. downloaded the Dockerfile in a new directory.
2. docker build . -t matthi17/debian-networkutilities #use your image name

Upload to Docker Hub

docker push matthi17/debian-networkutilities:latest #use your repo name
