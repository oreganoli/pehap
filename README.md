# Pehap

Pehap is a docker-compose template for the following environment:

- PHP
- Nginx
- MariaDB
- PHPMyAdmin

# Setup and use

Clone this repository.  
Install [Podman](https://podman.io) and podman-compose.  
This template should in theory work with vanilla Docker tooling, but Podman is recommended.  
Create an `.env` file and populate it:
```
MYSQL_ROOT_PASSWORD={whatever}
MYSQL_DATABASE={whatever}
MYSQL_USER={whatever}
MYSQL_PASSWORD={whatever}
```
Develop your PHP apps and place your static files in the `www` directory. The normal web server will run on port 8080; PMA will be available on port 8081.  
MySQL will keep its data in `datadir`.  
To run the environment, execute the following commands:
```bash
$ podman-compose pull
$ podman-compose up -d
```
To shut the environment down, use :
```bash
$ podman-compose down
```
## Licensing

Do whatever you want with this.