# NGINX + FPM example

Steps:

```sh
docker build -t php-fpm -f Dockerfile.php-fpm .

docker-compose up -d
docker-compose logs -f

curl http://localhost:8080/info.php

docker-compose down
```

Notes:
- For this simple demo, creating a custom image for FPM is not necessary.  You can just update the `docker-compose.yml` file to use the image `php:7.2-fpm` directly.  I added a custom image as an example for installing additional dependencies and php extensions (e.g. to access mysql).

Credits:
- [Creating a simple PHP-FPM, Nginx and MySQL application with docker compose](http://www.inanzzz.com/index.php/post/zpbw/creating-a-simple-php-fpm-nginx-and-mysql-application-with-docker-compose)