# rails-dev-env

Development environment for Rails based on docker and docker-compose

This repo contains Dockerfile and docker-compose.yml files
that allow for local development using docker and docker-compose.

Gems and node modules are installed inside a docker volume.

Postgres is used and it's data is stored inside a docker volume.

## Setup

It requires a .env file with two variables in it - UID and GID.
This ensures that the user running inside the container, is the same as the user on the host.
This eliminates any issues with file permissions
``` bash
echo "UID=$(id -u)" >> .env
echo "GID=$(id -g)" >> .env
docker-compose build
```
