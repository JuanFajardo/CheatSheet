# Git

## Creando Repositorio

### Inicio 
```bash
git init
git add --all
git commit -m "build: commit inicial"
git add origin hthttps://github.com/JuanFajardo/CheatSheet
git push -u origin main
```

### Commit normal
```bash
git add .
git commit -m "build: mensaje del commit"
git psuh -u origin main
```

### Commit vacio
```bash
git commit --allow-empty -m "chore: commit vacio"
git psuh -u origin main
```



## Ver Historial
```bash
git log
git log --oneline
git log -p <archivo>
git blame <archivo>
```


## Usuarios

### Ver usuario y correo
```bash
git config user.name
git config user.email
```

### Asignar Usuario y Correo
```bash
git config --global user.name "Juan Fajardo"
git config --global user.email "bett0@potosi.bo"
```

### Listar configuracion
```bash
git config -l
```


## DESCARGAR CAMBIOS (PULL)
```bash
git pull origin [Rama]

#Permitir fusion
git pull origin [Rama] --allow-unrelated-historie
```



## Estado

### Estados
```bash
git status
git status -s
git status -b
```






## CABECERA

### Agregar
```bash
# Agregar todo
git add .

# Agregar un archivo
git add [File]

# Agregar una carpeta
git add Carpeta/Carpeta1/.
```

### Remover Eliminar

## Remover
```bash
# Remover el ultimo commit
git reset HEAD~1

# Remover un archivo del head
git reset HEAD [hash_commit]

# Remover un archivo del stage
git checkout -- [archivo]

# Eliminar archivos recursvio de stage
git rm -r --cached .
```

## Eliminar
```bash
# Eliminar del repositorio
git rm [Archivo]

# Eliminar Recursivo
git rm -r [Carpeta]

# Eliminar Forzado
$ git rm -f [Archivo]
```



## COMMIT

__Cambiar el ultimo commit__
```bash
$ git commit --amend
```

__Temporal__
```bash
$ git checkout 0d1d7fc32
```

__Forzado__
```bash
$ git reset --hard 0d1d7fc32
```

__Deshacer el ultimo commit__
```bash
$ git reset --soft HEAD~1
$ git reset --merge
```




## CONEXION REMOTA

__Ver conexion remota__
```bash
$ git remote -v
```

__Ver informacion__
```bash
$ git config --list
```


__Ver Nombre__
```bash
$ git config user.name
```


__Ver Correo__
```bash
$ config user.name
```


__Agregar la conexion remota__
```bash
$ git remote add origin ssh://bett0@192.168.1.109:/home/bett0/Sistema/
```

__Cambiar la conexion remota__
```bash
$ git remote set-url origin ssh://bett0@192.168.1.109:/home/bett0/Sistema/
```



## CAMBIOS DEL PROYECTO

__Ver todo__
```bash
$ git diff [Archivo]
```

__Ver un archivo__
```bash
$ git diff --name-only [Archivo]
```

__Ver estado stage/head__
```bash
$ git diff --name-status [Archivo]
```


## ENVIAR CAMBIOS (PUSH)

__Enviar cambios__
```bash
$ git push origin [Rama]
```




## RAMAS

```bash
# Creando rama
git branch [rama]

# Elminar rama sin perder nada
git branch -d [rama]

# Elminar rama como macho alfa
git branch -D [ramama]

# Ver ramas
git branch

#Cambiando rama
git checkout [rama]

#Cambiar y crear una rama
git checkout -b [rama]
```


## Garbage Collet
### Recolector de Basura(Eliminar Basura)
```bash
#Recolector normal
git gc

#Recolector optimizado
git gc --aggressive
```


## Merge

### Fusion
```bash
git merge [rama]

# Simple con Master
git merge master

# Instalando Meld
PATH=$PATH:/c/python26
git config --global merge.tool meld
git config --global mergetool.meld.path /c/Users/andarno/Downloads/meld-1.5.2/bin/meld
```

### Diferencia
```bash
# Ver la diferencia entre ramas
git difftool  [Rama]

#Merge con las modificaciones necesarias
git mergetool
```




## Conexion Remota

```bash
# Generando el par de claves.
ssh-keygen

# Ver la clave publica
# Copiar en
# https://github.com/settings/keys
cat ~/.ssh/id_rsa.pub

# Crear el agente
eval `ssh-agent -s`

# Agregar la conexion
ssh-add id_rsa

# Test de conexion
ssh -T git@github.com
```

## Convencion Commit

```bash
#Nueva Funcionlidad: feat
git commit -m "feat: add user authentication"

#Correcion de error o bug: fix
git commit -m "fix: resolve login issue on mobile"

#Cambio en documentacion: docs
git commit -m "docs: update README documentation"

#Cambio con el formato: style
git commit -m "style: format code with Prettier"

#Cambio de mejora de estructura: refactor
git commit -m "refactor: simplify user validation logic"

#Agregacion de pruebas: test
git commit -m "test: add unit tests for login service"

#Cambios sin afectacion al codigo: chore
git commit -m "chore: update dependencies"

#Cambios que afectan al Sistema: build
git commit -m "build: update webpack configuration"

#Cambios en el CI/CD: ci
git commit -m "ci: update GitHub Actions workflow"

#Cambios para mejorar el rendimiento:perf
git commit -m "perf: optimize image loading on homepage"

#Desahcer algun commit 
git commit -m "revert: revert commit 123abc"

#Cambiso en el entorno virtual: env
git commit -m "env: update staging environment variables"

#Cambios en la configuracion:config
git commit -m "config: update ESLint rules" 

#Cambios o parches de seguridad:security
git commit -m "security: fix XSS vulnerability"
```



