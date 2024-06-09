# Task: Set Up a CI/CD Pipeline with Docker, Jenkins, and GitHub

## Prerequisites
1. Install Docker on your machine.
2. Set up a GitHub account.
3. Jenkins on Docker.

## Steps
### 1. Customize docker image to run jenkins on Docker ( need to install docker client on jenckins ).
    # build image 
    docker build -t jenkins-jdk11 .
    
    # run image
    docker run -d --name jenkins-docker --user root -p 8080:8080 -p 50000:50000 -v /var/run/docker.sock:/var/run/docker.sock jenkins-jdk11


### 2. Create a Sample Application
- Create a simple Node.js application.

### 3. Dockerize the Application
- Create a Dockerfile to containerize your application.

### 4. Push the Application to GitHub
- Create a new repository on GitHub and push your application code.

### 4. Set Up Jenkins
- Install necessary plugins for GitHub and Docker.
- Create a Jenkins pipeline to build and deploy the Docker container.


