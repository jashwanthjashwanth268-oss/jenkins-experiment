pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Create File') {
            steps {
                // Creates a file and writes text into it
                bat 'echo This is the content of the output file > output.txt'
            }
        }
        stage('Display Content') {
            steps {
                // Reads the file back to the console
                bat 'type output.txt' 
            }
        }
    }
}
