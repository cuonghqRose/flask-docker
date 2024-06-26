pipeline {
    agent agent
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/cuonghqRose/flask-docker.git'
            }
        }
        stage('docker') {
            steps {
                withDockerRegistry(credentialsId: 'hqcuongvt2012', url: 'https://index.docker.io/v1/') {
                  sh 'docker build -t hqcuong2012/cuonghq:v1 .'
                  sh 'docker push hqcuong2012/cuonghq:v1'
                }
            }
        }
    }
}