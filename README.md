# thiago-studier
Thiago Studier | Site de apresentação

COMANDOS: 
- npm install -g vue-cli //INSTALAR VUE
- vue init webpack social
- - cd social
- - npm run dev

- npm run build //PARA COMPILAR CODIGO PARA PRODUÇÃO
- php -S localhost:8000 //PARA RODAR A PASTA DIST EM UM SERVIDOR PHP

## Instalar laravel
- composer create-project --prefer-dist laravel/laravel webservice "5.5.*"

### após o gitclone para trazer a pasta vendor
- composer update

### instalar laravel/passport
- composer require laravel/passport

### migrate
- php artisan migrate

### configurar passport no projeto
- php artisan passport:install

### adicionar no User.php:
- use Laravel\Passport\HasApiTokens
- use HasApiTokens, HasFactory, Notifiable;

### no config/auth
- 'driver' => 'passport' no api

### install axios - dentro do frontend
- npm install axios --save
- import axios from 'axios' 