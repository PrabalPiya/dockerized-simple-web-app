# Dockerized Simple Web Application

This is a beginner-friendly DevOps project where I containerized a simple Node.js Express web application using Docker.

The goal of this project is to understand the basic DevOps workflow of packaging an application into a Docker image and running it as a container locally.

## Tools Used

* Node.js
* Express.js
* Docker
* VS Code
* Git/GitHub
* Terminal

## Architecture

```text
Developer writes application code
→ Dockerfile is created
→ Docker image is built
→ Docker container is started
→ Application runs on localhost
→ Logs and health endpoint are used for verification
```

## Folder Structure

```text
devops-docker-basic-app/
│
├── app/
│   ├── package.json
│   ├── server.js
│
├── Dockerfile
├── .dockerignore
└── README.md
```

## How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd devops-docker-basic-app
```

### 2. Build the Docker Image

```bash
docker build -t devops-basic-app:v1 .
```

### 3. Run the Docker Container

```bash
docker run -d -p 3000:3000 --name devops-basic-container devops-basic-app:v1
```

### 4. Test the Application

```bash
curl http://localhost:3000
```

Health check:

```bash
curl http://localhost:3000/health
```

### 5. Check Container Logs

```bash
docker logs devops-basic-container
```

### 6. Stop and Remove the Container

```bash
docker stop devops-basic-container
docker rm devops-basic-container
```

## What I Learned

* How to create a simple Node.js web application
* How to write a Dockerfile
* How to build a Docker image
* How to run a Docker container
* How port mapping works in Docker
* How to check container logs
* How to add a basic health check endpoint
* How to troubleshoot common Docker issues
