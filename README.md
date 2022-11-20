# PHP-Postgres-Nginx-Composer

docker compose setup Nginx 17.1 | PHP 8.1.1 | MySQL 8

Docker & Docker Compose configurations for PHP development.  
This setup comes with:

- PHP 8.1.1
- Nginx (1.17-alpine)
- MySQL 8
- Composer 2.2.4

# Requirements

- [Docker Engine](https://www.docker.com)
- [Docker Compose](https://docs.docker.com/compose/install/)

# Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/dockfiles/PHP-MYSQL-Nginx-Composer.git Docker-Lemp
```

cd into the new directory

```bash
cd Docker-Lemp
```

### 2. Ready for development!

- To start the LEMP server use this command:

```bash
docker compose up -d
```

- Go to `localhost:8000` on your web browser and you should see the PHP info page.

- The project root folder is the `public` directory.

- To stop the LEMP server use this command:

```bash
docker compose down
```

# Database Login

You can access the database on port `3306` of your host machine by using an app such as [dbeaver](https://dbeaver.io/).  
Some default credentials are set in `docker-compose.yml`

- Default MySQL user: root
- MYSQL_ROOT_PASSWORD: password
- MYSQL_DATABASE: database

# Running Composer Commands

To run composer commands, prefix the command with `docker compose`

Examples:

```bash
docker compose composer require nesbot/carbon
```

```bash
docker compose composer update
```
