# Docker Php Environment 2023
It provides basic PHP environment by using Docker Compose. Included services are, NGINX, PHP 8.2 or above, MariaDB and PHPMyAdmin.

## Usage

To get started, make sure you have Docker Desktop installed (https://www.docker.com/products/docker-desktop/) on your system, and then clone this repository.

Place all your code in the app directory present on the root of cloned repository. NGINX root directory path is app/public, So best practise is to place your code in the app and publically accessible files in the public folder.

Next, navigate in your terminal to the directory you cloned this, and spin up the containers for the web server by running `docker-compose up -d`.

**Note**: Your MySQL database host name should be `mysql`, **not** `localhost`. The username and database should both be `tutorial` with a password of `secret`. 

Bringing up the Docker Compose network with `app` instead of just using `up`, ensures that only our site's containers are brought up at the start, instead of all of the command containers as well. The following are built for our web server, with their exposed ports detailed:

- **nginx** - `:80`
- **mysql** - `:3306`
- **php** - `:9000`
- **phpmyadmin** - `:8080`

To change php.ini configuration, edit the /docker/php/config/php.ini file. Have Fun!

