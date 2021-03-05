# VIM

## Apertura de documentos

__Abrir un documento__

```$ vim bett0.txt```

__Abrir varios documentos__

```$ vim bett0.txt bett1.txt bett2.txt```

__Abrir un documentoe encriptado__

```$ vim -x archivo.cryp```


## Modo ex

__Resaltar sintaxis del codigo__

```:sintax on```

__Enumerar lineas__

```:set number```

__Tabulacion de cuatro espacios__

```:set tabstop=4```

__Sangría automática__

```:set autoindent ```

__Salir previa confirmacion__

```:q```

__Salir sin alerta__

```:q!```

__Guardar__

```:w```

__Guardar salir__

```:wq```

__Llevar cursor a la linea__

```:12```

__Archivo siguiente__

```:n ```

__Archivo Anterior__

```:N```

__Inserta un fichero nuevo__

```:e /home/bett0/bett9.txt```

__Buffer de todos los archivos__

```:buffers```

__Ir al archivo nro 2__

```:buffer 2```


__Insertar contenido__

```:r /home/bett0/bett0.txt```

__Ejecuta un comando__

```:r! 'ls -la'```


__Sustituir todo con confirmacion__

```:%s/Antiguo/Nuevo/gc```

* ```y si```
* ```n no```
* ```a todo```
* ```q parar sustituir```
* ```l salir```
* ```Ctrl+e AvPag```
* ```Ctrl+y RePag```

__Finalizar guardar y salir__

```ZZ```


## Modo Insertar

__Insertar__
> ```i``` Insertar en el cursor

> ```I``` Inserta al inicio de la linea

> ```10i Esc + Enter``` Insertar 10 lineas

> ```10i PALABRA Esc``` Insertar 10 veces PALABRA

> ```a``` Insertar despues del cursor

> ```A``` Insertar al final del linea

> ```O``` Insertar linea blanca antes de la linea actual

> ```o``` Insertar linea blanca despues de la linea actual



AltGr + 4 Cambiar de Mayuscula a Miniscula y viceversa


Busqueda
? Busca Atras
/ Busca Adelante
n siguiente buesqueda
N anterior busqueda
Modo visual

Modo Comando
## Navegacion
$ Llevar curso al final de linea
^ Llevar curso al inicio de linea
H Llevar cursor al inicio de la pantalla
M Llevar cursor al medio de la pantalla
L Llevar cursor al medio de la pantalla
e|E Cursor adelante saltando por palabra
b|B Cursor atras saltando por palabra
gg Cursor al inicio del documento
GG Cursos al final del documento  
Ctrl+B RePag
Ctrl+F AvPag

Visual 
modo visual
v
Cortar toda la linea
dd

Corta el contenido de la linea
D

Corta la plabra
dw

db Cortar la palabra anterior
dd Cortar línea
d$ Cortar hasta el final de la línea
d^ Cortar hasta el inicio de la línea


:17,20d                -> Cortar líneas de la 17 a la 20

10 dd


10 x

cortar donde esta el cursor
x

cortar antes del cursor
X

y$ Copia de la posición actual al final de la línea

yw Copia de la opsición actual al final de la palabra

copiar a partir del cursor
yy|Y

Copiar 3 lineas o mas
3yy | Y


p pegar después del cursor
P pegar antes del cursor
u Deshace el último cambio
U Restaura línea



. repite el ultimo comando




El fichero .vimrc

set nocompatible
set number
set ruler
syntax on 



ctrl + g Informacion


:earlier 1h   <-- Volvemos el documento a como estaba hace 1 hora
:later 10m    <-- Ahora avanzamos 30 minutos (a como estaba hace 60-10=50m)


20w 	Avanzar 20 palabras.
3fx 	Avanzar el cursor a la tercera aparición de la letra x en la línea actual, desde la posición del cursor. 

