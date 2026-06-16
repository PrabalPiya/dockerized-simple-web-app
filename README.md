Dockerized Simple Web Application

A beginner-friendly DevOps project where I used Docker to run a simple Node.js Express web application inside a container.

This project helped me understand how an application is packaged using a Dockerfile, built into a Docker image, and run as a container locally.

Project Goal

The main goal of this project was to learn the basic Docker workflow:

Write application code
→ Create a Dockerfile
→ Build a Docker image
→ Run the image as a container
→ Access the app on localhost
→ Check logs and health endpoint
Tools Used
Tool	Purpose
Node.js	To run the backend application
Express.js	To create a simple web server
Docker	To containerize the application
VS Code	To write and manage the project files
Git & GitHub	To track and upload the project
Terminal	To run Docker and Git commands
Folder Structure
devops-docker-basic-app/
│
├── app/
│   ├── package.json
│   └── server.js
│
├── Dockerfile
├── .dockerignore
└── README.md
How to Run This Project
1. Clone the Repository
git clone <your-repository-url>
cd devops-docker-basic-app
2. Build the Docker Image
docker build -t devops-basic-app:v1 .
3. Run the Docker Container
docker run -d -p 3000:3000 --name devops-basic-container devops-basic-app:v1
4. Test the Application

Open this in your browser:

http://localhost:3000

Or test using terminal:

curl http://localhost:3000

Health check endpoint:

curl http://localhost:3000/health
5. Check Container Logs
docker logs devops-basic-container
6. Stop and Remove the Container
docker stop devops-basic-container
docker rm devops-basic-container
Screenshots

Add screenshots here after running the project.

Docker Image Build
Add screenshot of successful docker build
Running Container
Add screenshot of docker ps
Application Running in Browser
Add screenshot of localhost:3000
Health Check Endpoint
Add screenshot of /health endpoint
What I Learned

Through this project, I learned:

How to create a simple Express application
How to write a Dockerfile
How to build a Docker image
How to run a Docker container
How Docker port mapping works
How to check container logs
How to create a basic health check endpoint
Why Docker images need to be rebuilt after code changes