# Laboratory Activity 4: Cloud-Native Engineer

## Mission Overview
In this laboratory activity, I learned about the shift from traditional Virtual Machines to modern containerization technologies. I explored Docker as a cloud-native platform and deployed a containerized Nginx web server in a KillerCoda environment. This hands-on experience demonstrated how containers provide faster deployment, efficient resource usage, and simplified application management compared to traditional virtualization approaches.

## Objectives
- Differentiate between traditional Virtual Machines (VMs) and Containers
- Access and use a Docker-enabled cloud environment through KillerCoda Playground
- Execute fundamental Docker Command Line Interface (CLI) commands
- Pull, run, manage, and stop a containerized application (Nginx)
- Create professional technical documentation using Markdown
- Continue developing a well-organized GitHub Cloud Computing Portfolio

## Docker Commands Executed

### Checkpoint 3: Docker Verification
```bash
docker --version
docker ps
```

### Checkpoint 4: Pulling and Running Nginx
```bash
docker pull nginx
docker run -d -p 8080:80 nginx
curl http://localhost:8080
```

### Checkpoint 5: Container Lifecycle Management
```bash
docker ps
docker stop <CONTAINER_ID>
docker ps
docker rm <CONTAINER_ID>
```

## Skills Learned
- **Docker Fundamentals:** I learned how to verify Docker installation and understand the Docker environment architecture
- **Container Deployment:** I gained hands-on experience pulling container images from Docker Hub and running them with proper port mapping configuration
- **Container Management:** I mastered the complete container lifecycle, including starting, monitoring, stopping, and removing containers using Docker CLI commands
- **Cloud-Native Thinking:** I developed an understanding of how containerization differs from traditional virtualization and why it is the foundation of modern DevOps practices

## Challenges Encountered
- **Port Mapping Confusion:** Initially, I needed to understand why we map port 8080 on the host to port 80 inside the container, but I learned this is necessary because the container runs in isolation and needs explicit port forwarding to be accessible
- **Container ID Management:** I had to identify the correct container ID for stopping and removing containers, which required using `docker ps` to list running containers before performing lifecycle operations
- **Terminal Output Interpretation:** Reading Docker command outputs and understanding what each field meant (STATUS, PORTS, NAMES) took practice but is now clear
