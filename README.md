# Jenkins + Docker CI/CD Pipeline

## 📌 Project Overview

This project demonstrates a basic **CI/CD pipeline using Jenkins and Docker**.

Jenkins automatically builds, tests, creates a Docker image, and deploys the Node.js application in a Docker container.

## 🛠️ Technologies Used

* Node.js
* Jenkins
* Docker
* Git
* GitHub

## 📂 Project Structure

```text
jenkins-pipeline/
├── server.js
├── package.json
├── Dockerfile
├── Jenkinsfile
└── README.md
```

## 🔄 CI/CD Pipeline

The Jenkins pipeline performs these steps:

1. Checkout the code from GitHub
2. Install Node.js dependencies
3. Run tests
4. Build the Docker image
5. Run the application in a Docker container

## ▶️ Run Locally

Build the Docker image:

```bash
docker build -t node-jenkins-app .
```

Run the container:

```bash
docker run -d --name node-jenkins-app -p 3000:3000 node-jenkins-app
```

Open in browser:

```text
http://localhost:3000
```

Expected output:

```text
Hello from Jenkins + Docker!
```

## 🚀 Jenkins Pipeline

Jenkins is configured to use the `Jenkinsfile` from the GitHub repository.

The pipeline automatically:

```text
GitHub
   ↓
Jenkins
   ↓
Install Dependencies
   ↓
Run Tests
   ↓
Build Docker Image
   ↓
Deploy Docker Container
```

## 🎯 Objective

The main objective of this project is to understand the basics of **CI/CD automation using Jenkins and Docker**.

## 👨‍💻 Author

**Dharani Kumar**
