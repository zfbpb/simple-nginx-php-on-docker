# Simple Demo: Nginx + PHP on Docker
This Docker project sets up a simple web development environment with two services:

* server: It uses the Nginx web server based on the stable Alpine Linux image. Nginx is exposed on port 8000 of the host machine and serves web content from the './src' directory, which is mounted to '/var/www/html' in the container. Additionally, it utilizes a custom Nginx configuration provided in './nginx/nginx.conf' by mapping it to '/etc/nginx/conf.d/default.conf' in the container.

* php: This service builds a custom PHP environment using a Dockerfile located in the './dockerfiles' directory. It also mounts the same './src' directory into the '/var/www/html' directory within the container with a 'delegated' volume configuration.

Together, these services create a development environment for serving PHP web applications using Nginx as the web server.

## Prerequisites
Before proceeding, make sure you have the following prerequisites installed on your system:
* [Docker](https://www.docker.com/): Make sure Docker is installed and running on your machine.

## Installation
* Clone this repo
```
   cd (project directory)
   docker compose up -d
   
   docker compose down
```
