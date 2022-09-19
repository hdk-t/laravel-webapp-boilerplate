# laravel-webapp-boilerplate
## Over View
A boilerplate for easily building a Laravel + MySQL web application execution environment

## Container Environment
- Application  
    - Laravel - 9.30.1  
    - PHP - 8.0.21  
    - Nginx - 1.22.0  
- Database
    - MySQL - 8.0.27  

## Host Required
- Docker
- Docker Compose  
- Git  

## Setup
### Copy .env
    cp -p ./src/.env.example ./src/.env

### Launch the containers
    docker-compose up -d

### Install library
    docker exec -it laravel9-webapp-boilerplate_app_1 composer install

### Generate APP_KEY
    docker exec -it laravel9-webapp-boilerplate_app_1 php artisan key:generate

### Acccess laravel wellcomepage
http://localhost:8080
