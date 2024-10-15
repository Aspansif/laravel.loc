## Установка из репозитория

Склонируйте репозиторий.
```sh
git clone https://github.com/Aspansif/larave.loc.git
```
Перейдите в папку с проектом и установите composer-зависимости
```sh
cd laravel.loc 
composer install
```
Скопируйте файл .env.example в .env
``` sh
cp .env.example .env
```

Сгенерируйте ключ шифрования 

``` sh
php artisan key:generate
```

измените файл конфигурации .env (если используете БД mysql)

``` php
DB_CONNECTION=sqlite
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=Имя_БД
DB_USERNAME=Ваш_логин
DB_PASSWORD=Ваш_пароль

Session_Driver=file
```

## Пустой проект создан командами
```sh
composer create-project laravel/laravel .
php artisan install:api
$ php artisan config:publish cors
$ php artisan storage:link
```

В корне проекта создан файл .htaccess
```php
RewriteEngine on
RewriteRule ^(.*)$ public/$1 [L]
```
