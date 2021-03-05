# i3wm


Actualizar el repositorio en Debian e instalar el gestor de ventanas i3

```bash
# apt update
# apte install i3
```

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


__Pantalla completa __

```[ $mod + f  ]```

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

```bash
$ i3-config-wizard

$ nano $HOME/.i3/config
$ nano $HOME/.config/i3/config
```

__Bloqueo de pantalla__

```bash
$ vim $HOME/.config/i3/config
bindsym $mod+shift+x exec i3lock
```

__Habilitar comandos de Multimedia__
```bash
# apt install playerctl
$ vim $HOME/.config/i3/config
https://faq.i3wm.org/question/3747/enabling-multimedia-keys/?answer=3759#post-id-3759
```

__Ejecutar vlc__

```bash
$ vim $HOME/.config/i3/config
exec vlc
exec_always vlc
```

__Habilitar la opacidad__

```bash
# apt install compton

$ compton --opacity-rule 45:'class_g *= "X-terminal-emulator"'

$ vim $HOME/.config/i3/config
exec compton --opacity-rule 50:'class_g *= "X-terminal-emulator"'
```

__Poner Fondo de Pantalla__

```bash
# apt install feh
$ feh --bg-scale wallpaper.jpg

$ vim $HOME/.config/i3/config
exec_always feh --bg-scale $HOME./wallpaper.jpg
```

__Resolucion de Pantalla__

```bash
# apt install arandr xrandr
$ arandr

$ vim $HOME/.config/i3/config
exec_always xrandr config.sh
```

__Poner o asignar nombre al EspacioDeTrabajo(workspace)__

```bash
$ vim $HOME/.config/i3/config
set $workName "nombre"
workspace --> name and move
```

__Poner Iconos al titulo de los EspaciosDeTrabajo(workspace)__

https://github.com/FortAwesome/Font-Awesome/releases

```bash
$ wget https://github.com/FortAwesome/Font-Awesome/releases/download/5.13.0/fontawesome-free-5.13.0-web.zip
$ cd Descargas/Font-Awesome-5.13.0/fonts/
$ mkdir $HOME/.fonts
$ mv cd Descargas/Font-Awesome-5.13.0/fonts/*.ttf  $HOME/.fonts

$ vim $HOME/.config/i3/config
set $workName "Nombre LOGOFIREFOX"
```
