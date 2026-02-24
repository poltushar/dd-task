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

Nginx routes traffic to frontend and backend.
