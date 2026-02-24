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
