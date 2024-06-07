pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/YOUR_USERNAME/simple-app.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('simple-app')
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('simple-app').run('-p 80:80')
                }
            }
        }
    }
}
