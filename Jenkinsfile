pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Interactive Input') {
            steps {
                script {
                    // This asks for a value while the pipeline is running
                    env.USER_CONFIRM = input(
                        message: 'Please confirm',
                        parameters: [string(name: 'CONFIRM_CODE', defaultValue: 'Approved', description: 'Type "Approved" to continue')]
                    )
                }
            }
        }
        stage('Verify Approval') {
            steps {
                bat "echo The user entered: ${env.USER_CONFIRM}"
            }
        }
    }
}
