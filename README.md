DevOps Project 1: Dockerized Simple Web App

This is a small beginner DevOps project where I used Docker to run a simple Node.js and Express web application inside a container.

The main goal of this project was to understand how an application is packaged using a Dockerfile, built into a Docker image, and then run as a container on my local machine.

Tools Used
Node.js
Express.js
Docker
VS Code
Git and GitHub
Terminal
Project Flow
Write application code
→ Create a Dockerfile
→ Build a Docker image
→ Run the image as a container
→ Access the app on localhost
→ Check logs and health endpoint
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
3. Run the Container
docker run -d -p 3000:3000 --name devops-basic-container devops-basic-app:v1
4. Test the App

Open this in your browser:

http://localhost:3000

Or test it using curl:

curl http://localhost:3000

Health check endpoint:

curl http://localhost:3000/health
5. Check Container Logs
docker logs devops-basic-container
6. Stop and Remove the Container
docker stop devops-basic-container
docker rm devops-basic-container
What I Learned

From this project, I learned the basic Docker workflow:

How to create a simple Express application
How to write a Dockerfile
How to build a Docker image
How to run an application inside a Docker container
How Docker port mapping works
How to check container logs
How to use a simple health check endpoint
Why code changes need a new image build