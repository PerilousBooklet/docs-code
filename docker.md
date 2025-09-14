# Docker

## Update a container in production

1. Stop container: `cd ../services/service_name`, `sudo docker-compose stop`
2. Remove old container: `sudo docker rm container_name`
3. Get new image and restart container: `sudo docker-compose up -d`

## Example: base

Repo: https://codeberg.org/simonrepp/feber

`Dockerfile`

```
FROM archlinux:base

USER root

WORKDIR /opt/feber

RUN pacman -Syu --needed --noconfirm php
# Enable PHP module: intl
RUN touch /etc/php/conf.d/intl.ini && \
    echo 'extension=/usr/lib/php/modules/intl.so' > /etc/php/conf.d/intl.ini

RUN mkdir -vp /opt/feber

COPY ./src/index.php /opt/feber/index.php
COPY ./src/scripts.js /opt/feber/scripts.js
COPY ./src/styles.css /opt/feber/styles.css
COPY ./src/favicon.svg /opt/feber/favicon.svg
COPY ./src/splash.jpg /opt/feber/splash.jpg

EXPOSE 9090

CMD php --server 0.0.0.0:9090 --docroot /opt/feber
```

`docker-build.sh`

```
#!/bin/bash
sudo docker build --tag simonrepp:feber-1.0.0 .
```

`docker-compose.yaml`

```
services:
  feber:
    image: simonrepp:feber-1.0.0
    ports:
      - 9090:9090
    volumes:
      - ./src:/opt/feber
```

`start.sh`

```
#!/bin/bash
docker-compose up -d
```
