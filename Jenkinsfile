pipeline {
    agent any
    parameters {
        string(name: 'USERNAME', defaultValue: 'Guest', description: 'Enter your name')
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Store User Data') {
            steps {
                // Note the use of double quotes for variable expansion in the bat command
                bat "echo ${params.USERNAME} > user.txt"
            }
        }
        stage('Verify Storage') {
            steps {
                bat 'type user.txt'
            }
        }
    }
}
