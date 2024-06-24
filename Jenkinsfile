pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/cuonghqRose/flask-docker.git'
            }
        }
        // stage('docker') {
        //     steps {
        //         withDockerRegistry(credentialsId: 'b797e772-8fdb-4527-9578-bc531cfbdf93', url: 'https://index.docker.io/v1/') {
        //           sh 'docker build -t cuonghq/jenkins:v1 .'
        //           sh 'docker push cuonghq/jenkins:v1 .'
        //         }
        //     }
        // }
    }
}