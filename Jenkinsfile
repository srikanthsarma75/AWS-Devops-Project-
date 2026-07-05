pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t employee-app:v1 .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker rm -f employee-container || true'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d --name employee-container -p 80:5000 employee-app:v1'
            }
        }
    }
}
