# NGINX + FPM example

Steps:

```sh
docker build -t php-fpm -f Dockerfile.php-fpm .

docker-compose up -d
docker-compose logs -f

curl http://localhost:8080/info.php

docker-compose down
```
