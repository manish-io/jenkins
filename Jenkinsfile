pipeline {
    agent any
    environment {
        DOCKER_IMAGE = 'my-app'
        DOCKER_TAG = "${env.BUILD_ID}"
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/manish-io/jenkins.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("${DOCKER_IMAGE}:${DOCKER_TAG}")
                }
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
