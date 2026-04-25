pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                bat 'python --version'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                bat 'python exp.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                echo 'App is live!'
            }
        }
    }

    post {
        success {
            echo ' Build Passed! No errors!'
        }
        failure {
            echo ' Build Failed! Fix the error!'
        }
    }
}