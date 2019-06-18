i3wm

# apt update
# apte install i3

Cerrar sesion

[ ENTER | YES ]

cerrar
[ win+shift+qq ]

abir
[ win + d ]

Abrir la terminal
[ win + Enter]

Abrir la terinal vertical
[ win + v + Enter]

Abrir la terminal horizontal
[ win + h + Enter]

Movere de una ventana a otra
[ win + Flechas ]

Pantalla completa la ventana seleccionada
[ win + s ]

Pantalla Dividida 
[ win + e ]

Listar en la barra
[ win + w ]

redimensionar
[ win + r]

mover la ventana
[ win + shitf + fle chas]

mover de area de trabajo
[ win + shitf + numeros]

cerrar sesion
[ win + shitf + e ]

Bloquear Pantalla
$ i3lock -i fondo.png
$ i3lock -t fondo.png -b -f

=====================================
Configuracion

$ i3-config-wizard
$ nano $HOME/.i3/config
$ nano $HOME/.config/i3/config

$vim $HOME/.config/i3/config
bindsym $mod+shift+x exec i3lock

Riniciar i3
[ win + shift + r ]

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
































