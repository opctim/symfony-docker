# 🐳 Docker + PHP 8.1 + MariaDB + Nginx + Symfony 6.1 Boilerplate

## Description

This is a complete stack for running Symfony 6.1 in Docker containers using `docker-compose`.

It is composed by 3 containers:

- `nginx`, acting as the webserver.
- `php`, the PHP-FPM container with the 8.1 version of PHP.
- `db` which is the MariaDB database container with a **MariaDB 10.10** image.

## Installation

1. 😀 Clone or download this repo.

2. In your project root, run `docker-compose up -d`

3. You should work inside the `php` container.

4. Inside the `php` container, run `composer install` to install dependencies from `/var/www/symfony` folder.

5. Use the following value for the DATABASE_URL environment variable:

```
DATABASE_URL=mysql://root:your_secret_password@db:3306/app_db?serverVersion=mariadb-10.10.2
```

You can change the database and nginx settings in the `.env` file at the root of the project. This file is meant to be tracked by git.
