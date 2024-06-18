pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    sudo docker build -t my-docker-image -f Dockerfile .
                }
            }
        }
    }
}
