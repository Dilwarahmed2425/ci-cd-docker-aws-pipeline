# 🚀 CI/CD Pipeline Automation using GitHub Actions, Docker & AWS EC2

## 📌 Project Overview

This project demonstrates an end-to-end CI/CD pipeline for a Dockerized Node.js application using **GitHub Actions**, **Docker**, **Docker Hub**, and **AWS EC2**.

Whenever code is pushed to the **main** branch, GitHub Actions automatically builds the Docker image, pushes it to Docker Hub, connects to an AWS EC2 instance through SSH, and deploys the latest version of the application. This eliminates manual deployment and ensures a consistent and reliable release process.

---

## 🏗️ Architecture

```
Developer
     │
     ▼
GitHub Repository
     │
     ▼
GitHub Actions
     │
     ├── Checkout Source Code
     ├── Build Docker Image
     ├── Push Image to Docker Hub
     └── Deploy to AWS EC2
                  │
                  ▼
         Pull Latest Docker Image
                  │
                  ▼
        Restart Docker Container
                  │
                  ▼
      Application Available on EC2
```

---

## 🛠️ Technologies Used

* Git
* GitHub
* GitHub Actions
* Docker
* Docker Hub
* AWS EC2
* Ubuntu Linux
* Node.js
* SSH

---

## 📂 Project Structure

```
ci-cd-pipeline-automation/
│
├── .github/
│   └── workflows/
│       └── deploy.yml
│
├── Dockerfile
├── app.js
├── package.json
├── .gitignore
└── README.md
```

---

## ⚙️ CI/CD Workflow

The pipeline is automatically triggered whenever code is pushed to the **main** branch.

Workflow Steps:

1. Checkout the latest source code
2. Set up Docker Buildx
3. Authenticate with Docker Hub
4. Build Docker image
5. Push Docker image to Docker Hub
6. Connect to AWS EC2 using SSH
7. Pull the latest Docker image
8. Stop and remove the existing container
9. Start a new container with the updated image

---

## 🔐 GitHub Secrets

The following GitHub repository secrets are used:

| Secret          | Description                      |
| --------------- | -------------------------------- |
| DOCKER_USERNAME | Docker Hub Username              |
| DOCKER_PASSWORD | Docker Hub Personal Access Token |
| EC2_HOST        | AWS EC2 Public IP                |
| EC2_USER        | EC2 Username                     |
| EC2_KEY         | Private SSH Key                  |

---

## 🐳 Docker Commands

Build Docker Image

```bash
docker build -t <dockerhub-username>/cicd-node-app .
```

Push Docker Image

```bash
docker push <dockerhub-username>/cicd-node-app:latest
```

Run Docker Container

```bash
docker run -d -p 80:3000 <dockerhub-username>/cicd-node-app:latest
```

---

## 🚀 Deployment Process

* Developer pushes code to GitHub.
* GitHub Actions automatically starts the workflow.
* Docker image is built.
* Image is pushed to Docker Hub.
* GitHub Actions connects to AWS EC2 using SSH.
* EC2 pulls the latest Docker image.
* Existing container is replaced.
* Updated application becomes available.

---

## ✨ Features

* Automated CI/CD pipeline
* Docker containerization
* Automated deployment to AWS EC2
* Secure GitHub Secrets management
* Zero manual deployment
* Fast and repeatable deployments

---

## 📚 Skills Demonstrated

* CI/CD Pipeline Automation
* GitHub Actions
* Docker
* Docker Hub
* AWS EC2
* Linux Administration
* SSH Automation
* Git Version Control
* DevOps Best Practices

---

## 🔮 Future Improvements

* Add automated unit testing
* Integrate code quality checks
* Deploy with Docker Compose
* Configure Nginx Reverse Proxy
* Add HTTPS using Let's Encrypt
* Add monitoring with Prometheus and Grafana

---

## 👨‍💻 Author

**Dilwar Ahmed**

GitHub: https://github.com/dilwarahmed

---

⭐ If you found this project helpful, feel free to star the repository.
