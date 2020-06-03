# LARAVEL

## Requisitos de Librerias

```bash
# apt install git curl php php-gd php-mbstring php-xml php-tokenizer php-mdb2 php-mysql php-pgsql

# apt install php libapache2-mod-php php-mbstring php-xmlrpc php-soap php-gd php-xml php-cli php-zip
```


## Instalacion Laravel

```bash
$ composer create-project --prefer-dist laravel/laravel [proyecto]
```

## Instalacion Laravel Version

```bash
$ composer create-project --prefer-dist laravel/laravel [proyecto] "x.x"
```

## Instalacion desde el repositorio

```bash
$ git clone https://github.com/laravel/laravel.git
$ cd laravel
$ composer install
```

## Instalacion de Base de Datos MariaDB

```bash
# apt install mariadb-server mariadb-client openssh-server openssh-client
```

### Configuracion basica de MariaDB

```bash
# mariadb -u root -p
```

```sql
> ALTER USER 'root'@'localhost' IDENTIFIED BY '123';
> CREATE DATABASE basedatos;
> grant all on *.* to 'bett0'@'localhost' identified by '123';
```

```bash
# systemctl restart mysql
```


## Instalacion de Base de Datos PostgreSQL

```bash
# apt install postgresql-server postgresql-client pgadmin3
```

### Configuracion basica de PostgreSQL

```bash
# su postgres
$ psql -U postgres -W
```

```sql
> \password postgres
> CREATE DATABASE basedatos;
```

```bash
# systemctl restart postgresql
```


## Composer

```bash
# apt install curl
$ curl -sS https://getcomposer.org/installer | php
# mv composer.phar /usr/local/bin/composer
# chmod +x /usr/local/bin/composer

$ source ~/.bashrc
$ composer -v

```


### Comandos basicos para ejecutar
```bash
$ cd laravel

$ chown -R bett0.bett0 laravel
$ chmod -R 755 laravel
$ chmod -R 777 laravel/storage

$ mv .env.example .env
$ php artisan key:generate

$ php artisan migrate:seed
```





## ARTISAN  

### Modelos

```bash
$ php artisan make:model [Modelo]
```

### Modelos en Carpeta
```bash
$ php artisan make:model [ModelosCarpeta]/[Carpeta]/[Modelo]
```

### Modelo con migracion

```bash
$ php artisan make:model [Modelo] -m
```  
### Controladores

```bash
$ php artisan make:controller [ModeloController] --clean / --resource
```

### Controladores  en Carpeta

```bash
$ php artisan make:controller [Carpeta]/[ModeloController]
```

### Migracion

```bash
$ php artisan migrate  migrate:reset / migrate:refresh
```

### Migracion Archivo especifico

```bash
$ php artisan migrate --path="/[Direccion]/"
```

### Migracion con datos

```bash
$ php artisan migrate --seed
```

### Insertar datos

```bash
$ php artisan db:seed
```

### Listar rutas

```bash
$ php artisan route:list
```

### Limpiar cache

```bash
$ php artisan cache:clear
```

### Generar Key

```bash
$ php artisan key:generate
```


## Sistema de Autentificacion

### Instalacion

```bash
$ php artisan make:auth
```

### Cambio de email por username (AuthenticatesUsers.php)

```php
return property_exists($this, 'username') ? $this->username : 'email';
return property_exists($this, 'username') ? $this->username : 'username';
```

### Restrinccion de EMAIL (AuthController.php)

```php
    return Validator::make($data, [
            'name' => 'required|max:255|unique:users',
            'email' => 'required|max:255',
            'password' => 'required|min:6|confirmed',
    ]);
```

### Creacion de Usuarios (AuthController.php)

```php
    return User::create([
            'name' => $data['name'],
            'nivel' => $data['nivel'],
            'email' => $data['email'],
            'password' => bcrypt($data['password']),
    ]);
```

### Aumentando datos Migracion (anio_mes_dia_create_users_table.php)

```php
    $table->increments('id');
    $table->string('name')->unique();
    $table->string('nivel');
    $table->string('email');
    $table->string('password');
```

### Aumentando datos Modelo (User.php)

```php
    protected $fillable = [
        'name', 'nivel', 'email', 'password',
    ];
```

For Laravel 5:
    Rename server.php in your Laravel root folder to index.php
    Copy the .htaccess file from /public directory to your Laravel root folder.


## PDF

### Instalacion

```bash
  composer require barryvdh/laravel-dompdf
```

### config/app.php

__Providers__

```php
  Barryvdh\DomPDF\ServiceProvider::class,
```

__Aliases__

```php
  'PDF' => Barryvdh\DomPDF\Facade::class,
```

__Link__
  https://github.com/barryvdh/laravel-dompdf

### Salto de pagina

```html
<div style="page-break-after:always;"></div>
```



## HTML
### Instalacion

```bash
$ composer require laravelcollective/html
```

```bash
$ composer require "laravelcollective/html":"^5.2.0"
```
### config/app.php

__Providers__

```php
  Collective\Html\HtmlServiceProvider::class,
```
__Aliases__

```php
  'Form' => Collective\Html\FormFacade::class,
  'Html' => Collective\Html\HtmlFacade::class,
```  
__Link__

  https://laravelcollective.com/docs/5.2/html
