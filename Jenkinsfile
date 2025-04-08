pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                // Since the code is already checked out by Jenkins, no need to re-clone it
                echo 'Code already checked out by Declarative SCM. Skipping extra git clone.'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'ls -l'
                sh 'docker build -t my-docker-webapp .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8081:80 my-docker-webapp'
            }
        }
    }
}
