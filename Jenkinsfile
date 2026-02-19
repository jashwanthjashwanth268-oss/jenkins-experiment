pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Manual Approval') {
            steps {
                // This will pause the pipeline and show a button
                input message: 'Proceed with Build?', ok: 'Yes, Proceed'
            }
        }
        stage('Post-Approval') {
            steps {
                echo "The build has been approved and is continuing..."
            }
        }
    }
}
