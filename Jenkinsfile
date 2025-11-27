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
        // Windows: use bat
        bat 'docker build -t sample-website .'
      }
    }

    stage('Deploy') {
      steps {
        // stop & remove old container if exists, then run new one on host:8081 -> container:80
        bat 'docker stop sample-container || exit 0'
        bat 'docker rm sample-container || exit 0'
        bat 'docker run -d --name sample-container -p 8081:80 sample-website'
      }
    }
  }

  post {
    success { echo 'Deployed: http://<host>:8081' }
    failure { echo 'Pipeline failed — check console output' }
  }
}
