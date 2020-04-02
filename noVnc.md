https://github.com/novnc/noVNC

# apt install x11vnc

$ x11vnc -storedpasswd

$ x11vnc -userpw -forever




$ git clone https://github.com/novnc/noVNC.git

$ cd noVNC

$ ./utils/launch.sh --vnc localhost:5901



# apt install novnc websockify python-numpy -y

$ x11vnc -passwd [123] -forever

$ websockify -D --web=/usr/share/novnc 6080 localhost:5900
