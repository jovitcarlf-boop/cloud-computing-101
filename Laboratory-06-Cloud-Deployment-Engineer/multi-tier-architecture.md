# Multi-Tier Architecture

## What is a Two-Tier Architecture?
A two-tier architecture divides an application into two layers: a web/application tier that users interact with, and a database tier that stores the application's data. Each tier has its own responsibility, and the two communicate over a network. In this laboratory, Nextcloud is the web/application tier and MariaDB is the database tier.

## The Web/Application Tier
The web/application tier is responsible for serving the user interface and handling HTTP requests from users. It processes user actions such as logging in, uploading files, and sharing folders, and it asks the database tier for the data it needs. In this deployment, the Nextcloud container fills this role and is exposed to the browser through port 8080.

## The Database Tier
The database tier is responsible for storing persistent data such as user accounts, credentials, and file metadata. It receives queries from the application tier and returns the results. In this deployment, the MariaDB container fills this role and is not exposed directly to users.

## Why Separate Them?
Separating the web server and the database into two containers allows each one to be updated, scaled, restarted, or fixed independently without affecting the other. It also improves security and stability, because a problem in the web container does not automatically corrupt or expose the database. Keeping one service per container also follows container best practices and makes the system easier to maintain and troubleshoot.
