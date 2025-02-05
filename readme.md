# MariaDB Docker

[**DockerHub Repository Link**](https://hub.docker.com/repository/docker/registryhj/mariadb/general)

<br />

## Supported Tags

- [`11.6`](https://hub.docker.com/repository/docker/registryhj/mariadb/tags/11.6/sha256-aa3c5c88383b5996c7ae61200817b1c433692bc9430bc494498d97d5209a2a8c) (`11.6.2-noble`, `latest`)
- [`11.4`](https://hub.docker.com/repository/docker/registryhj/mariadb/tags/11.4/sha256-e8c4c9c1c4a865a530eb6cf30f06b69eed9f825eefd499afc9f783a9b0fdbd6f): (`11.4.4-noble`, `lts`)
- [`11.2`](https://hub.docker.com/repository/docker/registryhj/mariadb/tags/11.2/sha256-547ea292b7bebd82f9cb8daca9fae574997bab03e8353f3be8e162d7d191c0a6): (`11.2.6-jammy`)
- [`10.11`](https://hub.docker.com/repository/docker/registryhj/mariadb/tags/10.11/sha256-19ef48ed41de4e20c2481bf1bb664e4ca053bf7cc8ad88b73cf57b236df91041): (`10.11.10-jammy`)

<br />

## How to use

**Pull this image:**

```
docker pull registryhj/mariadb:<tag_name>
```

**Create container in background process:**

```
docker run -d \
    --name <container_name> \
    -p <port>:3306 \
    -e MARIADB_ROOT_PASSWORD=<password> \
    registryhj/mariadb:<tag_name>
```

or (if you want to set `User`):

```
docker run -d \
    --name <container_name> \
    -p <port>:3306 \
    -e MARIADB_ROOT_PASSWORD=<password> \
    -e MARIADB_USER=<user> \
    -e MARIADB_PASSWORD=<password> \
    registryhj/mariadb:<tag_name>
```

or (if you want to set `Database`):

```
docker run -d \
    --name <container_name> \
    -p <port>:3306 \
    -e MARIADB_ROOT_PASSWORD=<password> \
    -e MARIADB_USER=<user> \
    -e MARIADB_PASSWORD=<password> \
    -e MARIADB_DATABASE=<database> \
    registryhj/mariadb:<tag_name>
```

**Execute Shell Prompt:**

```
docker exec -it <container_name> zsh
```

**Execute MariaDB Prompt:**

```
docker exec -it <container_name> mariadb -u root -p
```

or (if you set `--env MARIADB_USER=<user>`):

```
docker exec -it <container_name> mariadb -u <user> -p
```

<br />

## Supported Architectures

- `linux/amd64`
- `linux/arm64`

# <br />

Copyright © 2025 RegistryHJ
