# 🚀 End-to-End CI/CD Pipeline Using Jenkins, Docker & GitHub Webhooks  
### A Complete DevOps Automation Project for Interview Showcase

This project demonstrates a fully automated **CI/CD pipeline** built using **Jenkins, Docker, GitHub Webhooks, and Ngrok**.  
Whenever code is pushed to GitHub, a webhook triggers Jenkins, which automatically builds a Docker image, deploys the latest version of the website, and makes it publicly accessible.

This is a perfect hands-on DevOps project to showcase in interviews.

---

## 🌟 Project Overview

This project automates the entire workflow from code commit to deployment:

1. **Git push → GitHub Webhook Trigger**  
2. **Webhook → Jenkins Pipeline Activation**  
3. **Jenkins → Pulls Latest Code**  
4. **Jenkins → Builds Docker Image**  
5. **Jenkins → Runs Updated Docker Container**  
6. **Ngrok → Exposes Application to the Public Internet**

This setup reflects real-world DevOps CI/CD practices with continuous deployment.

---

## ⚙️ Technology Stack

| Technology | Purpose |
|-----------|---------|
| **HTML/CSS** | Website frontend |
| **Docker** | Containerization |
| **Jenkins** | CI/CD automation engine |
| **GitHub Webhooks** | Automatic pipeline triggering |
| **Ngrok** | Public URL tunneling |
| **VS Code** | Code editor |

---
Developer (You)
|
| 1. Commit & Push Code
v
GitHub Repository
|
| 2. GitHub Webhook Trigger
v
Jenkins Server
|
| 3. Pull Latest Code
| 4. Build Docker Image
| 5. Stop & Remove Old Container
| 6. Run Updated Container
v
Docker Engine
|
| 7. Expose Port via Ngrok
v
Public URL (Accessible Anywhere)


---

## 🛠 Jenkins Pipeline Steps (Jenkinsfile Breakdown)

### ✔ 1. Checkout Source Code  
Jenkins fetches the latest version from the GitHub repo.

### ✔ 2. Build Docker Image
```sh
docker build -t sample-website .


**###✔ 3. Stop & Remove Previous Container**

## 📂 Project Structure

