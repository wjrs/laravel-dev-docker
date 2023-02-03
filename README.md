## About Laravel with Docker environment

This project helps to create everything you need to start a fresh docker environment for Laravel (includes php-fpm, mariadb, redis, composer)

### Build containers

In the project root folder run:

`docker-compose build`

`docker-compose up -d`

### For a new Laravel project

Execute commands bellow to start a fresh installation inside the src folder

`docker exec -it app bash`

`composer create-project laravel/laravel . `

*You need to create project files inside the src folder to correct works or change the root folder in nginx config file.*

Access http://localhost:8080 on the browser and enjoy!

### For a existing Laravel project

Execute commands bellow to clone your existing project

Enter in `src` folder and run a clone of your project:

`cd src`

`git clone https://github.com/laravel/laravel.git . `

*You need to clone project files inside the src folder to correct works or change the root folder in nginx config file.*

Enter on container app and run a composer to install dependencies

`docker exec -it app bash`

`composer install`

Configure `.env` with correct container params.

Access http://localhost:8080 on the browser and enjoy!