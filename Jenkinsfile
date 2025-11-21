pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t mywebsite .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker rm -f mywebsite || exit 0'
                bat 'docker run -d --name mywebsite -p 8081:80 mywebsite'
            }
        }
    }
}
