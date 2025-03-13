pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main', url: 'https://github.com/Vaishnaviivn/PES1UG22CS669_Jenkins.git'
            }
        }
        stage('Build application') {
            steps {
                sh 'g++ -wrongflag -o  PES1UG22CS669-1 main.cpp'
            }
        }
        stage('Test application') {
            steps {
                sh './PES1UG22CS669-1'
            }
        }
        stage('Deploy application') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}
