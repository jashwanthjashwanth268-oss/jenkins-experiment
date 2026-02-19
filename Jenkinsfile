pipeline {
    agent any
    parameters {
        string(name: 'MESSAGE', defaultValue: 'Verification Test', description: 'Enter a message')
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('System Date') {
            steps {
                bat 'date /t' // Displays current system date in Windows
            }
        }
        stage('Verify Parameter') {
            steps {
                echo "Re-verifying parameter: ${params.MESSAGE}"
            }
        }
    }
}
