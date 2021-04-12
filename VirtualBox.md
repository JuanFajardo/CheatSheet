# Virtual Box

__Instalar Guest Aditions__

# apt-get install linux-source linux-headers-generic
dkms build-essential odule-assistant

__Pantalla a 16:9 fullscreen__

$ xrandr
$ cvt 1920 1080 [resolucion del monitor]
$ xrandr --newmode "1920x1080_60.00" 173.00 1920 2048 2248 1080 1083 1088 1120 -hsync +vsync
$ xrandr --addmode VBOX0 "1920x1080_60.00"
$ xrandr --ouput VBOX0 --mode "1920x1080_60.00"


__Solucion error SubSistema USB__


# usermod -a -G vboxusers USER
