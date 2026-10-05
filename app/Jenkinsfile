pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t node-jenkins-app:latest .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker stop node-jenkins-app || true'
                sh 'docker rm node-jenkins-app || true'
                sh 'docker run -d --name node-jenkins-app -p 3000:3000 node-jenkins-app:latest'
            }
        }
    }

    post {
        success {
            echo 'Application built and deployed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}