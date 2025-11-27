pipeline {
  agent any

  stages {
    stage('Checkout') { steps { checkout scm } }

    stage('Build Docker Image') {
      steps { sh 'docker build -t sample-website .' }
    }

    stage('Stop Old Container') {
      steps {
        sh 'docker stop sample-container || true'
        sh 'docker rm sample-container || true'
      }
    }

    stage('Run New Container') {
      steps { sh 'docker run -d --name sample-container -p 8081:80 sample-website' }
    }
  }

  post {
    success { echo 'Deployment successful — site available on port 8081' }
    failure { echo 'Pipeline failed — check logs' }
  }
}
