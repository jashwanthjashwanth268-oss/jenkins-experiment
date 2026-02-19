pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Info') {
            steps {
                // BUILD_NUMBER is a built-in variable in Jenkins
                echo "Current Jenkins Build Number: ${env.BUILD_NUMBER}"
            }
        }
        stage('Status') {
            steps {
                echo "Status: Execution of build #${env.BUILD_NUMBER} is successful."
            }
        }
    }
}
