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

## Usage
### Copy .env
    cp -p ./src/.env.example ./src/.env

### Launch the containers
    docker-compose up -d

### Install library
    docker exec -it laravel-webapp-boilerplate_app_1 composer install

### Generate APP_KEY
    docker exec -it laravel-webapp-boilerplate_app_1 php artisan key:generate

### Acccess laravel wellcomepage
http://localhost:8080

## If you use x-debug
### Launch the containers
    docker-compose -f ./docker-compose.xdebug.yml up -d
    
### Add vscode configurations  
```js:./vscode/launch.json
"configurations": [
    {
        "name": "XDebug on alpine-laravel9-docker",
        "type": "php",
        "request": "launch",
        "port": 9003,
        "pathMappings": {
            "/opt/html": "{YOUR_WORKSPACE_PATH}/laravel-webapp-boilerplate/src"
        }
    }
]
```