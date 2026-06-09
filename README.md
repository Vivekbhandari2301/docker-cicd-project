# CI/CD Pipeline using GitHub Actions, Docker and AWS EC2

## Project Overview

This project demonstrates a complete CI/CD (Continuous Integration and Continuous Deployment) pipeline using GitHub Actions, Docker, and AWS EC2.

The application is a static website hosted inside a Docker container running on an AWS EC2 instance. Whenever changes are pushed to the GitHub repository, GitHub Actions automatically deploys the latest version of the application to the EC2 server.

---

## Technologies Used

* AWS EC2
* Docker
* Git
* GitHub
* GitHub Actions
* Nginx
* Linux
* SSH

---

## Project Architecture

Developer (VS Code)
↓
Git Push
↓
GitHub Repository
↓
GitHub Actions
↓
SSH Deployment
↓
AWS EC2
↓
Docker Container
↓
Nginx Web Server
↓
Live Website

---

## CI/CD Workflow

1. Developer updates the application code.
2. Changes are committed and pushed to GitHub.
3. GitHub Actions workflow is triggered automatically.
4. GitHub Actions connects to EC2 using SSH.
5. Latest code is pulled from GitHub.
6. Docker image is rebuilt.
7. Old container is removed.
8. New container is deployed.
9. Updated website becomes available automatically.

---

## Commands Used

### Build Docker Image

docker build -t myportfolio .

### Run Docker Container

docker run -d -p 80:80 --name myapp myportfolio

### Check Running Containers

docker ps

### Clone Repository

git clone https://github.com/Vivekbhandari2301/docker-cicd-project.git

### Push Changes

git add .
git commit -m "Updated website"
git push origin main

---

## GitHub Secrets

* EC2_HOST
* EC2_USER
* EC2_SSH_KEY

These secrets are used by GitHub Actions to securely connect to the EC2 instance.

---

## Features

* Automated deployment
* Docker containerization
* AWS cloud hosting
* GitHub Actions CI/CD
* Nginx web server
* SSH-based deployment

---

## Learning Outcomes

* Docker image creation and container management
* AWS EC2 deployment
* Linux server administration
* Git and GitHub workflows
* GitHub Actions automation
* SSH authentication using PEM keys
* Continuous Integration and Continuous Deployment
