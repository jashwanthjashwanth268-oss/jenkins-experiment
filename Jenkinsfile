pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Get User Text') {
            steps {
                script {
                    env.MY_TEXT = input(
                        message: 'Enter text to save',
                        parameters: [string(name: 'CONTENT', description: 'What should go in the file?')]
                    )
                }
            }
        }
        stage('Save to File') {
            steps {
                // This saves the text you typed into input_data.txt
                bat "echo ${env.MY_TEXT} > input_data.txt"
                bat 'type input_data.txt'
            }
        }
    }
}
