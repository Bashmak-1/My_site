pipeline {
    agent any
    stages {
        stage('Pull Latest Code') {
            steps {
                sh 'git pull origin main'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker compose build'
            }
        }
        stage('Restart Containers') {
            steps {
                sh 'docker compose up -d'
            }
        }
    }
}
