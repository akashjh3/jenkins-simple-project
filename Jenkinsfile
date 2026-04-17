pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/akashjh3/jenkins-simple-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-app:latest .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run --rm my-app:latest'
            }
        }
    }
}
