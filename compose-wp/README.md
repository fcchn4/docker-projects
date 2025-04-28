# Setup a Wordpress app on a docker-compose

## Solution

- [Docker Compose](https://docs.docker.com/compose/compose-file/compose-file-v3/)

### Version docker images

1. [Wordpress](https://hub.docker.com/_/wordpress?tab=description&page=3&ordering=last_updated)
    - 5.6.1
    - 5.6.1-apache
    - 5.6.1-fpm
    - 5.6.1-php7.4-fpm
    - 5.6.1-php7.4-apache
    - 5.6.1-php7.4
    - 5.6.1-php7.3
    - 5.6.1-php7.3-fpm
    - 5.6.1-php7.3-apache

2. Dababase 
    - [Mysql 5.7.33](https://hub.docker.com/_/mysql)
    - [MariaDB 10.5](https://hub.docker.com/_/mariadb)

### Commands

```bash
# Deploy project
$ docker-compose -f docker-compose-maridb.yml up
$ docker-compose -f docker-compose-mysql.yml up

# Stop Project
$ docker-compose -f docker-compose-maridb.yml up
$ docker-compose -f docker-compose-mysql.yml up

# Deploy project as demon
$ docker-compose -f docker-compose-maridb.yml up -d
$ docker-compose -f docker-compose-mysql.yml up -d
```