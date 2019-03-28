# NGINX + FPM example

Steps:

```sh
docker build -t php-fpm -f Dockerfile.php-fpm .

docker-compose up -d
docker-compose logs -f

curl http://localhost:8080/info.php

docker-compose down
```

Credits:
- [Creating a simple PHP-FPM, Nginx and MySQL application with docker compose](http://www.inanzzz.com/index.php/post/zpbw/creating-a-simple-php-fpm-nginx-and-mysql-application-with-docker-compose)