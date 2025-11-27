🚀 End-to-End CI/CD Pipeline Using Jenkins, Docker & GitHub Webhooks
A Professional DevOps Project for Interview Showcase

This project demonstrates a complete CI/CD pipeline built using Jenkins, Docker, GitHub Webhooks, and Ngrok.
Whenever I push code to GitHub, Jenkins automatically builds a Docker image, deploys the updated website, and makes it accessible publicly.

🌟 Project Summary

This project shows how I automated:

Git push → triggers GitHub webhook

Webhook → triggers Jenkins pipeline

Jenkins → pulls code, builds Docker image

Jenkins → runs container with new website

Ngrok → exposes website to the public

This is ideal for showcasing DevOps experience during interviews.

⚙️ Technology Stack

HTML/CSS

Docker

Jenkins

GitHub Webhooks

Ngrok

VS Code

📂 Project Structure
my-sample-website/
│── index.html
│── Dockerfile
│── Jenkinsfile
└── README.md

🔄 CI/CD Workflow
Developer (me)
     |
     | Push code
     v
GitHub Repo
     |
     | Webhook trigger
     v
Jenkins Pipeline
     |
     | Builds Docker image
     | Removes old container
     | Starts new container
     v
Docker Engine
     |
     | Exposed using Ngrok
     v
Public URL (for demo)

🛠 Jenkins Pipeline Steps
✔ 1. Checkout Code

Jenkins pulls the latest code from GitHub.

✔ 2. Build Docker Image
docker build -t sample-website .

✔ 3. Stop Previous Container
docker stop sample-container || true
docker rm sample-container || true

✔ 4. Run Updated Container
docker run -d --name sample-container -p 8080:80 sample-website

🌐 Public Exposure Using Ngrok

To allow others to view the website:

ngrok http 8080


Ngrok provides a public URL like:

https://xxxx-xxxx.ngrok-free.dev


Share this link with interviewers/friends.

🎯 Why This Project Is Useful for Interviews

This project demonstrates:

CI/CD automation

Jenkins pipeline writing skills

Docker containerization

GitHub webhook integration

End-to-end deployment workflow

Real DevOps hands-on implementation

Perfect to show practical DevOps skills.

🖋 Author

Yugendra Prasad
DevOps Engineer
GitHub: https://github.com/Yugendrarepo
