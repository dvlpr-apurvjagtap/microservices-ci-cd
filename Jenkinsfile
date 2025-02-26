pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', credentialsId: 'github-credentials', url: 'https://github.com/dvlpr-apurvjagtap/microservices-ci-cd.git'
            }
        }

        stage('Build Backend') {
            steps {
                sh 'docker build -t microservices-ci-cd-backend ./backend'
            }
        }

        stage('Build Frontend') {
            steps {
                sh 'docker build -t microservices-ci-cd-frontend ./frontend'
            }
        }

        stage('Test Docker Containers') {
            steps {
                sh 'docker images'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    }
}
