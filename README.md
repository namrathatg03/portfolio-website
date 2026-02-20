# 🐳 Static Website Deployment on AWS EC2 using Docker

## 📌 Project Overview
This project demonstrates how to containerize a static website using **Docker** and deploy it on an **AWS EC2** instance.  
The website is served using the **Nginx web server** inside a Docker container and accessed through the EC2 **public IP address**.

## 🛠️ Technologies Used
- HTML5
- Docker
- Nginx
- Amazon EC2
- Ubuntu 22.04 LTS
- Git & GitHub
- 
## 🎯 Features
- Simple static website
- Dockerized using Nginx
- Runs inside a Docker container
- Deployed on AWS EC2
- Accessible using public IP address

## 🚀 Steps Followed

### 1️⃣ Create Website Files
- Created a simple `index.html` file
- Tested the website locally in the browser

### 2️⃣ Create Dockerfile
- Used official **nginx:alpine** image
- Copied website files into Nginx web directory
- Exposed port 80

### 3️⃣ Build and Run Docker Container Locally
- Built Docker image using Dockerfile
- Ran the container and verified output locally

### 4️⃣ Launch AWS EC2 Instance
- Created an EC2 instance using **Ubuntu 22.04 LTS**
- Enabled SSH (port 22) and HTTP (port 80) in security group

### 5️⃣ Install Docker on EC2
- Updated system packages
- Installed Docker engine
- Configured Docker permissions for the user

### 6️⃣ Deploy Website on EC2 using Docker
- Copied project files from local system to EC2
- Built Docker image on EC2
- Ran Docker container on port 80

## 🌍 Live Website
🔗 **EC2 Public IP URL:**  
http://54.227.90.155/

## 📸 Screenshots
- Dockerfile
- Docker build output on AWS
- Docker running container (`docker ps`)
- Website accessed using public IP
- EC2 instance running (AWS Console)

## 📚 Learning Outcomes
- Learned Docker containerization basics
- Understood Dockerfile and image creation
- Gained hands-on experience with AWS EC2
- Learned how to deploy containers on cloud virtual machines
- Understood basic DevOps deployment workflow

## Task 3 - CI/CD using GitHub Actions

In this task, GitHub Actions is used to automate Docker build and push process.

When code is pushed to the main branch:

1. Docker image is built automatically
2. Image is pushed to Docker Hub
3. The website is ready for deployment

Docker Image:
namrathatg/portfolio-website

To pull image:
docker pull namrathatg/portfolio-website:latest

To run container:
docker run -d -p 8080:80 namrathatg/portfolio-website
