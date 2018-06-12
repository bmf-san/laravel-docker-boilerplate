# Laravel Docker Boilerplate
This is a boilerplate for laravel working with docker.

# Features
- Laravel
- Docker
- Nginx
- Composer
- Nodejs

# Get Started
## Create a env file
```
cd src/laravel/
cp .env.example .env
```

## Setup the docker-compose
```
docker-compose build
docker-compose up -d
```

## Setup the backend-app
```
docker exec -it php /bin/sh -c "cd laravel && composer install"
docker exec -it php /bin/sh -c "cd laravel && npm cache verify && npm install"
docker exec -it php /bin/sh -c "cd laravel && php artisan key:generate"
docker exec -it php /bin/sh -c "cd laravel && php artisan migrate && php artisan db:seed"
```

## Add hosts settings to `/etc/hosts`
```
127.0.0.1 laravel-docker-boilerplate
```

# License
This project is licensed under the terms of the MIT license.

# Author
bmf - A Web Developer in Japan.
* [@bmf-san](https://twitter.com/bmf_san)
* [bmf-tech](http://bmf-tech.com/)
