# Git


__Nombre de Usuario y Correo__

```git
git config user.name
git config user.email
```

__Listar__

```git
git config -l
```

## Asignar datos generales
git config --global user.name "Juan Fajardo"
git config --global user.email "juanfajardo@potosi.bo"



# ESTADO
## Ver estado
git status

## Ver estado corto
git status -s

## Ver estado de Rama
git status -b





# AGREGAR A CABECERA

## Todo
git add .

## Un archivo
git add \[File\]

## Una carpeta
git add Carpeta/Carpeta1/.

## Remover de cabecera
git reset HEAD \[Archivo\]

## Remover un archivo del stage
git checkout -- \[Archivo\]

## Eliminar
### Del repositorio
git rm \[Archivo\]

### Eliminar Recursivo
git rm -r \[Carpeta\]

### Eliminar Forzado
git rm -f \[Archivo\]





# COMMIT
## Commit Largo
git commit -m

## Commit Corto
git commit -m "Nombre - Mensaje"

## Listar los cambios
git log --oneline

### Cambiar el ultimo commit
git commit --amend

### Temporal
git checkout 0d1d7fc32

### Forzado
git reset --hard 0d1d7fc32

### Deshacer el ultimo commit
git reset --soft HEAD~1
git reset --merge




# CONEXION REMOTA
## Ver conexion remota
git remote -v

## Agregar la conexion remota
git remote add origin ssh://bett0@192.168.1.109:/home/bett0/Sistema/

## Cambiar la conexion remota
git remote set-url origin ssh://bett0@192.168.1.109:/home/bett0/Sistema/





# CAMBIOS DEL PROYECTO
## Ver todo
git diff \[Archivo\]

## Ver un archivo
git diff --name-only \[ARCHIVo\]

## Ver estado stage/head
git diff --name-status \[ARCHIVo\]





# ENVIAR CAMBIOS\(PUSH\)
## Enviar cambios
git push origin \[Rama\]





# RAMAS
## Crear rama
git branch \[Rama\]

## Elminar rama sin perder nada
git branch -d \[Rama\]

## Elminar rama como macho alfa
git branch -D \[Rama\]

## Recolector de Basura
git gc

## Verificar rama
git branch

## Cambiando rama
git checkout \[Rama\]

## Fusionar/Merge
### Simple con Rama
git merge \[Rama\]

### Simple con Master
git merge master

### Instalando Meld
PATH=$PATH:/c/python26
git config --global merge.tool meld
git config --global mergetool.meld.path /c/Users/andarno/Downloads/meld-1.5.2/bin/meld

### difftool cuando queramos ver la diferencia entre ramas
git difftool  \[Rama\]

### mergetool cuando queramos hacer el merge con las modificaciones necesarias
git mergetool




# DESCARGAR CAMBIOS \(PULL\)
## Origin
git pull origin \[Rama\]

git pull origin \[Rama\] --allow-unrelated-historie

## Link
git pull ssh://bett0@192.168.1.109:/home/bett0/Sistema/ \[Rama\]

## Forzar
git gc
git reset HEAD \[File\]
git pull origin \[Rama\]
