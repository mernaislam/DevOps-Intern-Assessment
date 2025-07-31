# DevOps Internship Assessment

This repository contains the completed tasks for the DevOps Internship Assessment.

## ✅ Part 1 - Application Setup and CI/CD

### ✔️ Clone Repository
Cloned the original Node.js TODO List application from:
> https://github.com/Ankit6098/Todo-List-nodejs

### ✔️ MongoDB Configuration
- Created a new database on **MongoDB Atlas**.
- Updated the `.env` file with the correct connection string.

### ✔️ Dockerization
- Dockerized the Node.js app with a `Dockerfile` found in `nodejs-app - task 1`.
- Tagged the image and pushed it to a **private Docker registry**.

### ✔️ GitHub Actions - CI
- Implemented GitHub Actions workflow for Continuous Integration:
  - Build the Docker image.
  - Push the image to the private Docker registry on every push to the `main` branch.

---

## ✅ Part 2 - VM Provisioning with Ansible 

### ✔️ Virtual Machine
- Provisioned a **Linux EC2 instance** on AWS.

### ✔️ Ansible Configuration
- From the local machine, used **Ansible** to:
  - Install and configure Docker and Docker-compose.
  - Verify Docker installation and start the Docker service.

---

## ✅ Part 3 - Docker Compose and Auto-Updates 

### ✔️ Docker Compose Deployment
- Set up the application with `docker-compose.yml` on the VM found in `docker-compose task 3`.
- Included:
  - TODO Node.js application container.
  - MongoDB service.
  - Proper **health checks** for services.

### ✔️ Image Auto-Update
- Used **Watchtower** to enable automatic updates:
  - Continuously checks the private Docker registry for new image versions every 30 seconds.
  - Pulls the updated image and restarts the container when changes are detected.

### ✔️ Justification for Watchtower
- **Watchtower** is lightweight, easy to set up, and integrates well with Docker Compose.
- Automates update cycles without requiring additional orchestration.

---

##  Part 4 - Bonus

### ❗ Kubernetes and ArgoCD
- Kubernetes was used to deploy the app on the VM using `kubectl` and `Deployment` manifests found in `kube - task 4`.
- **ArgoCD was NOT implemented** due to time constraints.

---
