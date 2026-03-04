pipeline {
    agent any

    environment {
        APP_NAME = "my-app"
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Deploy Simulation') {
            steps {
                echo 'Simulating deployment...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
        always {
            echo 'Cleaning workspace...'
            cleanWs()
        }
    }
}