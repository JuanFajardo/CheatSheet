# Instalacion de noVNC

https://github.com/novnc/noVNC
https://github.com/novnc/websockify/wiki/Encrypted-Connections
https://openwebinars.net/blog/configurar-certificados-ssl-gratis-en-ubuntu-con-apache/

## Instalacion del x11vnc

```bash
# apt install x11vnc
$ x11vnc -storedpasswd
$ x11vnc -userpw -forever
```

## Instalacion de noVNC desde el repositorio
```bash
$ git clone https://github.com/novnc/noVNC.git
$ cd noVNC
$ ./utils/launch.sh --vnc localhost:5901
```

```bash
# apt install novnc websockify python-numpy -y
$ x11vnc -passwd [123] -forever
$ websockify -D --web=/usr/share/novnc 6080 localhost:5900
```

```bash
apt install x11vnc

x11vnc -storepasswd
x11vnc -usepw  &
netstat -putan | grep x11vnc
```
## Instalacion 

```bash
# apt update
# apt install novnc

$ git clone https://github.com/novnc/noVNC.git
$ cd noVNC
# openssl req -new -x509 -days 365 -nodes -out self.pem -keyout self.pem
# ./utils/launch.sh --vnc localhost:5901
```