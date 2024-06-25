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
                withDockerRegistry(credentialsId: '70103929-6f87-4ac2-b6b0-2c6634efca1a', url: 'https://index.docker.io/v1/') {
                  sh 'docker build -t hqcuong2012/cuonghq:v1 .'
                  sh 'docker push hqcuong2012/cuonghq:v1 .'
                }
            }
        }
    }
}