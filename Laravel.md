#LARAVEL 5.2
##Instalacion Laravel Ultima version
  composer create-project --prefer-dist laravel/laravel [Proyecto]
##Instalacion Laravel v5.2
  composer create-project --prefer-dist laravel/laravel [Proyecto] "5.2.*"

#ARTISAN  
##Modelos
  php artisan make:model [Modelo]
##Modelos en Carpeta
  php artisan make:model [ModelosCarpeta]/[Carpeta]/[Modelo]
##Modelo con migracion
  php artisan make:model [Modelo] -m
##Controladores
  php artisan make:controller [ModeloController]
##Controladores  en Carpeta
  php artisan make:controller [Carpeta]/[ModeloController]
##Migracion
  php artisan migrate
##Migracion Archivo especifico
  php artisan migrate --path="/[Direccion]/"
##Migracion con datos
  php artisan migrate --seed
##Insertar datos
  php artisan db:seed 
##Listar rutas
  php artisan route:list
##Limpiar cache
  php artisan cache:clear
##Sistema de Autentificacion
###Instalacion
  php artisan make:auth
###Cambio de email por username (AuthenticatesUsers.php)
  return property_exists($this, 'username') ? $this->username : 'email';
  return property_exists($this, 'username') ? $this->username : 'username';
###Restrinccion de EMAIL (AuthController.php)
    return Validator::make($data, [
            'name' => 'required|max:255|unique:users',
            'email' => 'required|max:255',
            'password' => 'required|min:6|confirmed',
    ]);
###Creacion de Usuarios (AuthController.php)
    return User::create([
            'name' => $data['name'],
            'nivel' => $data['nivel'],
            'email' => $data['email'],
            'password' => bcrypt($data['password']),
    ]);
###Aumentando datos Migracion (anio_mes_dia_create_users_table.php)
    $table->increments('id');
    $table->string('name')->unique();
    $table->string('nivel');
    $table->string('email');
    $table->string('password');
    
###Aumentando datos Modelo (User.php)
    protected $fillable = [
        'name', 'nivel', 'email', 'password',
    ];



#PDF
##Instalacion
  composer require barryvdh/laravel-dompdf
##config/app.php
###Providers
  Barryvdh\DomPDF\ServiceProvider::class,
###Aliases
  'PDF' => Barryvdh\DomPDF\Facade::class,
###Link
  https://github.com/barryvdh/laravel-dompdf
  
  
  

#HTML
##Instalacion
  composer require "laravelcollective/html":"^5.2.0"
##config/app.php
###Providers
  Collective\Html\HtmlServiceProvider::class,
###Aliases
  'Form' => Collective\Html\FormFacade::class,
  'Html' => Collective\Html\HtmlFacade::class,
###Link
  https://laravelcollective.com/docs/5.2/html