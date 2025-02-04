# MariaDB Docker Image

[**DockerHub Repository Link**](https://hub.docker.com/repository/docker/registryhj/mariadb/general)

<br />

## Supported Tags

- [`11.6`](https://hub.docker.com/repository/docker/registryhj/mariadb/tags/11.6/sha256-dea6df08ccacc3ab8c2aa926c0487b7c89635b347756dc1d1389b9d32c074083) (`11.6.2-noble`, `latest`)
- [`11.4`](https://hub.docker.com/repository/docker/registryhj/mariadb/tags/11.4/sha256-4bc6842f47994ba3b412564994c0097c4034130471fa749db6639a68132f07b0): (`11.4.4-noble`, `lts`)
- [`11.2`](https://hub.docker.com/repository/docker/registryhj/mariadb/tags/11.2/sha256-67a0fa28368912d5c8d5c34af33b7a86d54bf0a47a348adab866cb161ebe8af3): (`11.2.6-jammy`)
- [`10.11`](https://hub.docker.com/repository/docker/registryhj/mariadb/tags/10.11/sha256-b240ff74a8059503c5f73b012e034e3e69174f1891386430413f34fcac460321): (`10.11.10-jammy`)

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
