# Dockerized Node.js Application 🚀

## Overview
This project demonstrates building and containerizing a Node.js application using Docker and deploying it on AWS EC2. The application runs inside a Docker container and is accessible via the EC2 public IP.

---

## Tech Stack
- Node.js
- Express.js
- Docker
- AWS EC2
- Git & GitHub

---

## Features
- Simple Express-based Node.js application
- Dockerized application for consistent runtime
- Cloud deployment on AWS EC2
- Publicly accessible via EC2 public IP

---

## Project Structure

app.js - Main application file  
Dockerfile - Docker image configuration  
package.json - Dependencies and scripts  
.gitignore - Git ignored files  
.dockerignore - Docker ignored files  
README.md - Project documentation  

---

## Run Locally (Without Docker)

Install dependencies:

npm install

Start application:

npm start

Application runs on:

http://localhost:3000

---

## Run Using Docker (Local)

Build Docker image:

docker build -t docker-node-app .

Run container:

docker run -p 3000:3000 docker-node-app

Application runs on:

http://localhost:3000

---

## Deployment on AWS EC2 (Cloud Deployment)

This application is deployed on an AWS EC2 Ubuntu instance using Docker.

### Deployment Steps

1. Created AWS EC2 Ubuntu instance.
2. Opened required ports in Security Group:
   - Port 22 (SSH)
   - Port 3000 (Application)
3. Connected to EC2 using SSH.
4. Installed Docker on EC2 instance.
5. Cloned GitHub repository.
6. Built Docker image inside EC2.
7. Ran container exposing port 3000.
8. Accessed application via EC2 public IP.

---

### EC2 Commands Used

Install Docker:

sudo apt update
sudo apt install docker.io -y
sudo usermod -aG docker ubuntu

Clone repository:

git clone https://github.com/<your-username>/docker-node-app.git
cd docker-node-app

Build and run container:

docker build -t docker-node-app .
docker run -d -p 3000:3000 docker-node-app

---

## Access Application

http://<EC2-PUBLIC-IP>:3000

---

## Learning Outcomes
- Learned Docker containerization
- Hands-on AWS EC2 deployment
- Basic cloud deployment workflow
- Git and GitHub project management

---

## Author
DevOps / Cloud Practice Project
