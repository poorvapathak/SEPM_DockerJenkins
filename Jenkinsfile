pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                echo 'Code already checked out by Declarative SCM. Skipping extra git clone.'
            }
        }
        stage('Build Docker Image') {
            steps {
                bat 'dir'
                bat 'docker build -t my-docker-webapp .'
            }
        }
        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 8081:80 my-docker-webapp'
            }
        }
    }
}
