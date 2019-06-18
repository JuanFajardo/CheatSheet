# i3wm

~~~# apt update~~~

~~~# apte install i3~~~

Los siguientes comandos estan basados en el default de la instalacion de i3.


__Iniciar sesion__

```[ ENTER | YES ]```


__Cerrar Ventana__

```[ $mod + shift + qq ]```


__Abir Aplicacion__

```[ $mod + d ]```


__Abrir la terminal__

```[ $mod + Enter ]```


__Abrir la terinal vertical__

```[ $mod + v + Enter ]```


__Abrir la terminal horizontal__

```[ $mod + h + Enter ]```


__Movere de una ventana a otra__

```[ $mod + Flechas  ]```


__Pantalla completa la ventana seleccionada__

```[ $mod + s  ]```


__Pantalla Dividida__

```[ $mod + e  ]```


__Listar en la barra__

```[ $mod + w  ]```

__Redimensionar__

```[ $mod + r ]```


__Mover la aplicacion__

```[ $mod + shift + flechas ]```

__Mover de area de trabajo__

```[ $mod + shift + numeros ]```


__Cerrar Sesion__

```[ $mod + shift + e  ]```


__Reiniciar i3__

```[ $mod + Shift + r  ]```


__Bloquear Pantalla__

```$ i3lock -i fondo.png```
```$ i3lock -t fondo.png -b -f```

## Configuracion

__Comando para crear el archivo de configuración__
$ i3-config-wizard
$ nano $HOME/.i3/config
$ nano $HOME/.config/i3/config

$vim $HOME/.config/i3/config
bindsym $mod+shift+x exec i3lock


$vim $HOME/.config/i3/config
https://faq.i3wm.org/question/3747/enabling-multimedia-keys/?answer=3759#post-id-3759
apt install playerctl


$vim $HOME/.config/i3/config
exec vlc
exec_always vlc


apt install compton
compton --opacity-rule 45:'class_g *= "X-terminal-emulator"'
$vim $HOME/.config/i3/config
exec compton --opacity-rule 50:'class_g *= "X-terminal-emulator"'


apt install feh
feh --bg-scale wallpaper.jpg
$vim $HOME/.config/i3/config
exec_always feh --bg-scale $HOME./wallpaper.jpg


xrandr
apt install arandr
arandr
$vim $HOME/.config/i3/config
exec_always xrandr confi.sh


$vim $HOME/.config/i3/config
set $workName "nombre"
workspace --> name and move

$xprop
assign [class="Firefox-esr"] $workName



https://github.com/FortAwesome/Font-Awesome/releases
$ wget reales.zip
$ cd Descargas/Font-Awesome-5.0/fonts/
$ mkdir $HOME/.fonts
$ mv cd Descargas/Font-Awesome-5.0/fonts/*.ttf  $HOME/.fonts


$vim $HOME/.config/i3/config
set $workName "nombre LOGOFIREFOX"


=============================================


