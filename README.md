# opendigital-docker-wordpress
Repo for dockerfile to build common PHP Wordpress environment image

Available from the the docker hub registry as `openhealthdigital/wordpress`

Based on `openhealthdigital/php-apache` with additional wordpress command line tools installed.

Repo structure is based on the same version folder convention as official docker hub repos (e.g. php: https://github.com/docker-library/php)

Updates to dockerfiles are made to each "version" folder so that anyone using the docker image tagged 7.1 `openhealthdigital/wordpress:7.1` will get the latest updates to the docker image when they pull the image.

# Usage
* `docker run -v ./my-web-dir:/var/www openhealthdigital/wordpress:7.1`

# Use with docker compose:
`docker-compose.yaml`:
```
web:
  image: openhealthdigital/wordpress:7.1
  volumes:
    - ./my-web-dir:/var/www
```
* `docker-compose up web`
