pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Filipos123344/OURPROJECT.git'
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
