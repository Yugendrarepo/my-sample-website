pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Build') {
      steps {
        sh 'docker build -t sample-website .'
      }
    }

    stage('Deploy') {
      steps {
        // stop & remove old container if exists, then run new one on host:8081 -> container:80
        sh 'docker stop sample-container || true'
        sh 'docker rm sample-container || true'
        sh 'docker run -d --name sample-container -p 8081:80 sample-website'
      }
    }
  }

  post {
    success { echo 'Deployed: http://<host>:8081' }
    failure { echo 'Pipeline failed — check console output' }
  }
}
