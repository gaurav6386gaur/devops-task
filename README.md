
DevOps Task – Node.js Application Deployment with Jenkins & Docker

##  Overview
This repository contains a simple **Node.js application** that serves a static file.  
The app is containerized with **Docker** and deployed automatically using a **Jenkins pipeline**.

---

##  Setup & Deployment Guide

### 1. Clone Repository
```bash
git clone https://github.com/SwayattDrishtigochar/devops-task.git
cd devops-task
2. Build Docker Image
bash
Copy code
docker build -t node-app .
3. Run Docker Container
bash
Copy code
docker run -d --name node-app -p 3000:3000 node-app
4. Access Application
Open in browser:

cpp
Copy code
http://3.111.196.16:3000
