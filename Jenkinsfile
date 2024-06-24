pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/cuonghqRose/flask-docker.git'
            }
        }
        stage('docker') {
            steps {
                withDockerRegistry(credentialsId: '49857e66-8779-4221-abfb-0589b37de0ca', url: 'https://index.docker.io/v1/') {
                  sh 'docker build -t cuonghq/jenkins:v1 .'
                  sh 'docker push cuonghq/jenkins:v1 .'
                }
            }
        }
    }
}