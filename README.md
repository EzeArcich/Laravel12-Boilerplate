<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

<p align="center">
<a href="https://github.com/laravel/framework/actions"><img src="https://github.com/laravel/framework/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## Características

Detalle del enviroment:
 - PHP 8.2.28
 - Laravel 10
 - Mysql 8.0

## Indicaciones

Al clonar el repo, desde la raíz del proyecto, usamos el comando "composer install", luego "docker-compose up -d" para levantar los contenedores. Debemos ingresar al contenedor de Laravel, con el comando "docker exec -ti laravel_app bash", una vez dentro, corremos el comando "composer install" para instalar las dependencias, y luego las migraciones con "php artisan migrate". También ejecutamos "php artisan key:generate". Parados en el entorno local, raíz del proyecto, debemos ejecutar "npm install" y "npm run build", y con esto, ya nos dejará el proyecto corriendo en "http://localhost:8002/". El puerto obviamente se puede cambiar en el archivo docker-compose.yml, antes de levantar los contenedores.
Recordar también agregar un archivo .env, donde poner estos datos para la DB:

DB_CONNECTION=mysql
<br>
DB_HOST=laravel_db
<br>
DB_PORT=3306
<br>
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=root

En la rama "filament", encontrarán un boilerplate similar, sólo que con Filament. En caso de usar Filament tener en cuenta que se deben de correr los comandos de filament (para crear paneles, usuarios, etc) desde dentro del contenedor "laravel_app".

