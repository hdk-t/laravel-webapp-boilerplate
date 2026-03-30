# laravel-webapp-boilerplate
## Over View
A boilerplate for easily building a Laravel + MySQL web application execution environment

## Container Environment
- Application  
    - Frankenphp: 1
    - Laravel: 13
    - PHP: 8.5
- Database
    - MySQL: 8.0.27  

## Host Required
- Docker
- Docker Compose  
- Git  

## Usage
### Copy .env
    cp -p ./src/.env.example ./src/.env

### Launch the containers
    docker-compose up -d

### Install library
    docker exec -it laravel-webapp-boilerplate_app_1 composer install

### Permission settings
    docker exec -it laravel-webapp-boilerplate_app_1 chown -R www-data:www-data /app/storage /app/bootstrap/cache

### Generate APP_KEY
    docker exec -it laravel-webapp-boilerplate_app_1 php artisan key:generate

### Database Setting
    docker exec -it laravel-webapp-boilerplate_db_1 mysql -u root -ppass  
    mysql> GRANT ALL ON *.* TO user;  
    mysql> CREATE DATABASE test;  

### Acccess laravel wellcomepage
http://localhost
