# Docker Compose Guide

This guide explains the `docker-compose.yml` file used to deploy a two-tier Nextcloud private cloud, made up of a Nextcloud web container and a MariaDB database container.

## What does the `services:` block do?
The `services:` block defines every container that makes up the application. Each entry under it, such as `database` and `app`, is one service. For each service, Docker Compose reads the image, ports, and environment variables and creates and starts the matching container. In this file, `database` runs MariaDB 10.6 and `app` runs Nextcloud. Compose also places both services on a shared default network.

## How did the Nextcloud container find the database container?
The Nextcloud container found the database through the environment variable `MYSQL_HOST=database`. The value `database` is the name of the database service in the Compose file. Docker Compose automatically creates a private network for the stack and lets services reach each other by service name, so `database` resolves to the MariaDB container's address. Nextcloud also uses the same `MYSQL_DATABASE`, `MYSQL_USER`, and `MYSQL_PASSWORD` values that the MariaDB container uses to create its database and user, so the credentials match.

## What is the difference between `docker run` and `docker-compose up -d`?
`docker run` starts a single container, and every option (image, ports, environment variables, network) must be typed manually in the command. To run a multi-container application, each container and its network connection has to be set up separately, which is repetitive and error-prone.

`docker-compose up -d` reads a `docker-compose.yml` file and creates and starts all of the defined containers together, with their networking, in one command. The `-d` flag runs them in the background (detached). Because the configuration is saved in a file, the deployment is repeatable, easy to share, and can be stored in version control. This is the idea behind Infrastructure as Code (IaC).
