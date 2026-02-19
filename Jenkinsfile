pipeline {
    agent any
    parameters {
        string(name: 'MESSAGE', defaultValue: 'Hello world', description: 'Type something here')
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Print Message') {
            steps {
                echo "The message is: ${params.MESSAGE}"
            }
        }
        stage('Windows Command') {
            steps {
                bat 'echo Hello from Jenkins'
            }
        }
    }
}
