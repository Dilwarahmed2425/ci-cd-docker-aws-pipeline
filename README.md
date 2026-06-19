# 🚀 CI/CD Pipeline Automation using GitHub Actions, Docker & AWS EC2

## 📌 Project Overview

This project demonstrates a complete CI/CD (Continuous Integration and Continuous Deployment) pipeline for a Node.js application using GitHub Actions, Docker, Docker Hub, and AWS EC2.

Whenever code is pushed to the **main** branch, GitHub Actions automatically:

- Builds the Docker image
- Pushes the image to Docker Hub
- Connects to AWS EC2 using SSH
- Pulls the latest Docker image
- Stops and removes the existing container
- Deploys the latest application container automatically

This eliminates manual deployment and provides a fast, reliable deployment process.

---

# 🏗️ Architecture

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
     └── SSH into AWS EC2
                 │
                 ▼
          Pull Latest Docker Image
                 │
                 ▼
        Restart Docker Container
                 │
                 ▼
         Application Available
```

---

# 🛠️ Technologies Used

- Git & GitHub
- GitHub Actions
- Docker
- Docker Hub
- AWS EC2 (Ubuntu)
- Linux
- Node.js
- SSH

---

# 📁 Project Structure

```
ci-cd-pipeline-automation/
│
├── .github/
│   └── workflows/
│       └── deploy.yml
│
├── app.js
├── package.json
├── Dockerfile
├── .gitignore
└── README.md
```

---

# ⚙️ CI/CD Workflow

The pipeline is triggered automatically whenever code is pushed to the **main** branch.

Workflow Steps:

1. Checkout source code
2. Set up Docker Buildx
3. Login to Docker Hub
4. Build Docker image
5. Push Docker image to Docker Hub
6. Connect to AWS EC2 via SSH
7. Pull latest Docker image
8. Stop existing container
9. Remove old container
10. Deploy new container

---

# 🔐 GitHub Secrets Used

The following repository secrets are configured:

| Secret | Purpose |
|----------|----------|
| DOCKER_USERNAME | Docker Hub Username |
| DOCKER_PASSWORD | Docker Hub Access Token |
| EC2_HOST | EC2 Public IP |
| EC2_USER | EC2 Username |
| EC2_KEY | Private SSH Key |

---

# 🐳 Docker Commands Used

Build Image

```bash
docker build -t username/cicd-node-app .
```

Push Image

```bash
docker push username/cicd-node-app:latest
```

Run Container

```bash
docker run -d -p 80:3000 username/cicd-node-app
```

---

# 🚀 Deployment Process

1. Developer pushes code to GitHub.
2. GitHub Actions starts automatically.
3. Docker image is built.
4. Image is pushed to Docker Hub.
5. GitHub Actions connects to AWS EC2.
6. Latest Docker image is pulled.
7. Existing container is replaced.
8. Updated application becomes available.

---

# 📸 Screenshots

## GitHub Actions

_Add screenshot here_

```
screenshots/github-actions-success.png
```

---

## Docker Hub Repository

_Add screenshot here_

```
screenshots/dockerhub-image.png
```

---

## Running Container on EC2

_Add screenshot here_

```
screenshots/docker-ps.png
```

---

## Application Output

_Add screenshot here_

```
screenshots/application.png
```

---

# ▶️ How to Run Locally

Clone Repository

```bash
git clone https://github.com/your-username/ci-cd-pipeline-automation.git
```

Move into project

```bash
cd ci-cd-pipeline-automation
```

Build Docker Image

```bash
docker build -t cicd-node-app .
```

Run Container

```bash
docker run -d -p 3000:3000 cicd-node-app
```

Open Browser

```
http://localhost:3000
```

---

# 📈 Key Features

- Automated CI/CD pipeline
- Docker containerization
- Secure GitHub Secrets management
- Automatic deployment to AWS EC2
- Zero manual deployment steps
- Repeatable and reliable deployment process

---

# 📚 Skills Demonstrated

- CI/CD Automation
- GitHub Actions
- Docker
- Docker Hub
- AWS EC2
- Linux Administration
- SSH Automation
- Git Version Control
- DevOps Workflow

---

# 🔮 Future Enhancements

- Add automated testing before deployment
- Add rollback strategy
- Deploy using Docker Compose
- Add monitoring with Prometheus & Grafana
- Configure Nginx Reverse Proxy
- Add SSL using Let's Encrypt

---

# 👨‍💻 Author

**Dilwar Ahmed**

GitHub: https://github.com/dilwarahmed

---

⭐ If you found this project useful, consider giving it a Star!