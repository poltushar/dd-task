### MEAN Stack Application Deployment using Docker, CI/CD and AWS

## 📌 Project Overview

This project demonstrates containerization and deployment of a full-stack MEAN application using:

* MongoDB

* Express.js

* Angular

* Node.js

* Docker & Docker Compose

* AWS EC2 (Ubuntu)

* GitHub Actions (CI/CD)

* Nginx Reverse Proxy

The application is deployed on AWS EC2 and accessible using Port 80.

## Architecture Overview

1. Developer pushes code to GitHub.

2. GitHub Actions builds Docker images.

3. Images are pushed to Docker Hub.

4. CI/CD connects to AWS EC2 using SSH.

5. Latest images are pulled on EC2.

6. Docker Compose restarts containers.
### 🐳 Docker Setup

 ## Backend Dockerfile

* Base Image: node:18-alpine

* Exposes backend port

* Runs Express server
 ## Frontend Dockerfile
 
 * Uses node:18-alpine
   
 * Builds Angular application
   
 * Served using Nginx
### Database Setup
MongoDB is running as a Docker container using the official MongoDB image inside docker-compose.yml.

## AWS EC2 Setup

* Created Ubuntu EC2 instance (Free Tier).

## Opened ports:

 * 22 (SSH)

 * 80 (HTTP)

## Installed:

* Docker

* Docker Compose

* Nginx

Deployed application using docker-compose.
Nginx routes traffic to frontend and backend.

### CI/CD Pipeline (GitHub Actions)

`
.github/workflows/deploy.yml
`
### GitHub Secrets Used

* DOCKER_USERNAME

* DOCKER_PASSWORD

* EC2_HOST

* EC2_USER

* EC2_SSH_KEY

Secrets are stored securely in GitHub Actions.

### Screenshots 

The repository contains screenshots of:

* Successful GitHub Actions pipeline
  <img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/11eb5019-5277-4209-8df1-69ad61469138" />


* Docker image build and push logs

* Docker Hub image list

* Running containers (docker ps)

* Working application UI

* Nginx configuration

* AWS EC2 instance details

### How Deployment Works

Whenever code is pushed to the main branch:

1. GitHub Actions builds new Docker images.

2. Images are pushed to Docker Hub.

3. EC2 pulls latest images.

4. Containers are restarted automatically.

5. Application updates without manual intervention

### Application Access.

Frontend and Backend are accessible via:

`
http://13.232.72.59/tutorials
`

