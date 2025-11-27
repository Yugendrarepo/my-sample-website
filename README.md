# 🚀 My Sample DevOps Project – Fully Automated CI/CD with Jenkins, Docker & Ngrok

This project demonstrates a complete CI/CD pipeline using **Jenkins**, **Docker**, **GitHub Webhooks**, and **Ngrok** to showcase your DevOps skills during interviews.

---

## 📦 How the Project Works

### ✔ 1. GitHub Code Push  
Whenever you update or push code to GitHub, a **webhook** notifies Jenkins instantly.  

### ✔ 2. Jenkins Pipeline Execution  
Jenkins automatically:  
- Pulls the updated code  
- Builds a Docker image  
- Stops the old container  
- Deploys a new updated container  

### ✔ 3. Stop Previous Container
```bash
docker stop sample-container || true
docker rm sample-container || true
```

### ✔ 4. Run Updated Website Container
```bash
docker run -d --name sample-container -p 8080:80 sample-website
```

This ensures your latest website version is always live after each code change.

---

## 🌐 Public Exposure Using Ngrok

Run this command to make the site visible anywhere:

```bash
ngrok http 8080
```

Ngrok gives a URL like:

```
https://xxxx-xxxx.ngrok-free.dev
```

Share it with:  
- Recruiters  
- Interviewers  
- Friends  
- Teammates  

---

## 🎯 Why This Project Is Perfect for Interviews

This project shows real DevOps hands-on experience:

✔ Continuous Integration  
✔ Continuous Deployment  
✔ Jenkins pipeline setup  
✔ Docker containerization  
✔ GitHub Webhook automation  
✔ Real-time updates  
✔ Deployment orchestration  
✔ Building & managing Docker images  
✔ Using Ngrok for public demo  

---

## 💡 Key Highlights to Mention in Interviews

- Built a fully automated CI/CD pipeline using Jenkins  
- Configured GitHub Webhooks for automatic job triggering  
- Created Docker images on every code change  
- Automated container lifecycle management  
- Made the website publicly accessible using Ngrok  
- End-to-end DevOps workflow using real tools  

---

## 🧪 Sample Jenkinsfile (Reference)

```groovy
pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Yugendrarepo/my-sample-website'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t sample-website .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker stop sample-container || true'
                sh 'docker rm sample-container || true'
            }
        }

        stage('Run New Container') {
            steps {
                sh 'docker run -d --name sample-container -p 8080:80 sample-website'
            }
        }
    }
}
```

---

## 🛳 Sample Dockerfile (Reference)

```dockerfile
FROM nginx:alpine
COPY index.html /usr/share/nginx/html/index.html
```

---

## 👨‍💻 How to Run Locally

### 1. Clone the Repository
```bash
git clone https://github.com/Yugendrarepo/my-sample-website
```

### 2. Build the Docker Image
```bash
docker build -t sample-website .
```

### 3. Run the Docker Container
```bash
docker run -d --name sample-container -p 8080:80 sample-website
```

### 4. Open in Browser
```
http://localhost:8080
```

### 5. (Optional) Expose Publicly Using Ngrok
```bash
ngrok http 8080
```

---

## 🖋 Author  
**Yugendra Prasad**  
DevOps Engineer  

GitHub: https://github.com/Yugendrarepo
