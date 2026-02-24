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

 <img width="1918" height="1073" alt="image" src="https://github.com/user-attachments/assets/41a0b68e-8941-46ee-8e90-b9862e581798" />
 <img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/2f4c0a08-a98c-41ad-8f98-1c4076ad889b" />
 <img width="1917" height="1078" alt="image" src="https://github.com/user-attachments/assets/17952ab8-a5f5-4c22-8506-6119f17f14b3" />
 <img width="1855" height="1078" alt="image" src="https://github.com/user-attachments/assets/80ccd600-e01b-41b5-b3ef-b8a36c52ce45" />


* Docker Hub image list
<img width="1917" height="1078" alt="image" src="https://github.com/user-attachments/assets/628f7baa-d847-4f11-826a-a8eff8219af8" />

* Running containers (docker ps)
  <img width="1918" height="1077" alt="image" src="https://github.com/user-attachments/assets/6ff44691-5f50-4f71-b0c1-743bf8edd602" />


* Working application UI
  <img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/f8e19281-5ff7-401a-8927-82d04b72b491" />
  <img width="1918" height="1077" alt="image" src="https://github.com/user-attachments/assets/d1627555-4b87-4f48-b61e-17015d9bb17f" />
  <img width="1918" height="1076" alt="image" src="https://github.com/user-attachments/assets/204e810a-5497-4672-bb03-e344d23dabdf" />
  <img width="1918" height="1076" alt="image" src="https://github.com/user-attachments/assets/5b8745e2-85a5-4782-b605-5af514bc0c7c" />
  <img width="1918" height="1072" alt="image" src="https://github.com/user-attachments/assets/9094e567-8d67-4f90-9fc8-c9fb6e77b8b1" />






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

