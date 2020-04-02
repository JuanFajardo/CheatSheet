# Git


__Ver usuario y correo__
```git
$ git config user.name
$ git config user.email
```


__Asignar Usuario y Correo__
```git
$ git config --global user.name "Juan Fajardo"
$ git config --global user.email "juanfajardo@potosi.bo"
```

__Listar__
```git
$ git config -l
```



## ESTADO

__Ver estado__
```git
$ git status
```

__Ver estado corto__
```git
$ git status -s
```

__Ver estado de Rama__
```git
$ git status -b
```

## AGREGAR A CABECERA

__Todo__
```git
$ git add .
```

__Un archivo__
```git
$ git add \[File\]
```

__Una carpeta__
```git
$ git add Carpeta/Carpeta1/.
```

__Remover de cabecera__
```git
$ git reset HEAD [Archivo]
```

__Remover un archivo del stage__
```git
$ git checkout -- [Archivo]
```

__Refresacar archivo Git Ignore__
```git
$ git rm -r --cached .
$ git add .
$ git commit -m "GitIgnore Refresacado" 
```


## Eliminar
__Del repositorio__
```git
$ git rm [Archivo]
```

__Eliminar Recursivo__
```git
$ git rm -r [Carpeta]
```

__Eliminar Forzado__
```git
$ git rm -f [Archivo]
```



## COMMIT

__Commit Largo__
```git
$ git commit -m
```

__Commit Corto__
```git
$ git commit -m "Nombre - Mensaje"
```

__Listar los cambios__
```git
$ git log --oneline
```

__Cambiar el ultimo commit__
```git
$ git commit --amend
```

__Temporal__
```git
$ git checkout 0d1d7fc32
```

__Forzado__
```git
$ git reset --hard 0d1d7fc32
```

__Deshacer el ultimo commit__
```git
$ git reset --soft HEAD~1
$ git reset --merge
```




## CONEXION REMOTA

__Ver conexion remota__
```git
$ git remote -v
```

__Ver informacion__
```git
$ git config --list
```


__Ver Nombre__
```git
$ git config user.name
```


__Ver Correo__
```git
$ config user.name
```


__Agregar la conexion remota__
```git
$ git remote add origin ssh://bett0@192.168.1.109:/home/bett0/Sistema/
```

__Cambiar la conexion remota__
```git
$ git remote set-url origin ssh://bett0@192.168.1.109:/home/bett0/Sistema/
```



## CAMBIOS DEL PROYECTO

__Ver todo__
```git
$ git diff [Archivo]
```

__Ver un archivo__
```git
$ git diff --name-only [Archivo]
```

__Ver estado stage/head__
```git
$ git diff --name-status [Archivo]
```


## ENVIAR CAMBIOS (PUSH)

__Enviar cambios__
```git
$ git push origin [Rama]
```




## RAMAS


__Crear rama__
```git
$ git branch [Rama]
```

__Elminar rama sin perder nada__
```git
$ git branch -d [Rama]
```

__Elminar rama como macho alfa__
```git
$ git branch -D [Rama]
```

__Recolector de Basura__
```git
$ git gc
```

__Ver ramas__
```git
$ git branch
```

__Cambiando rama__
```git
$ git checkout [Rama]
```


## Fusionar/Merge

__Simple con Rama__
```git
$ git merge [Rama]
```

__Simple con Master__
```git
$ git merge master
```
__Instalando Meld__
```git
$ PATH=$PATH:/c/python26
$ git config --global merge.tool meld
$ git config --global mergetool.meld.path /c/Users/andarno/Downloads/meld-1.5.2/bin/meld
```

__Ver la diferencia entre ramas__
```git
$ git difftool  [Rama]
```
__Merge con las modificaciones necesarias__
```git
$ git mergetool
```


## DESCARGAR CAMBIOS (PULL)
__Origin__
```git
$ git pull origin [Rama]
$ git pull origin [Rama] --allow-unrelated-historie
```

