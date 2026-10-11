# Laboratory 06 - Cloud Deployment Engineer

## Mission Overview
In this mission, I worked as a Cloud Deployment Engineer at CloudNova Technologies. I moved from deploying single containers to deploying a multi-tier application using Docker Compose. I wrote a `docker-compose.yml` file that defines a Nextcloud web container and a MariaDB database container, then deployed the whole private cloud storage stack with a single command.

## Objectives
- Explain the concept of a multi-tier application architecture.
- Understand the purpose and structure of a `docker-compose.yml` file.
- Use the nano text editor to create configuration files.
- Deploy a multi-container application (Nextcloud + MariaDB) using Docker Compose.
- Document deployment procedures and Infrastructure as Code (IaC) principles using Markdown.
- Continue expanding my GitHub Cloud Computing Portfolio.

## Commands Executed
```bash
mkdir nextcloud-deployment
cd nextcloud-deployment
nano docker-compose.yml
docker-compose up -d
docker-compose ps
docker-compose down
```

## Screenshots
- Deployment: `screenshots/compose-deployment.png`
- Nextcloud web interface: `screenshots/nextcloud-web.png`
- Teardown: `screenshots/compose-teardown.png`

## Skills Learned
- Explaining two-tier (multi-tier) application architecture
- Writing a YAML configuration file with correct indentation
- Using the nano text editor in the Linux terminal
- Deploying and tearing down a multi-container application with Docker Compose
- Connecting containers by service name and configuring them with environment variables
- Accessing a containerized web application through a mapped port
- Documenting Infrastructure as Code (IaC) using Markdown
