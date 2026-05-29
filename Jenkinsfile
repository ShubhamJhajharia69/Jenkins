pipeline {
    agent any
    
    triggers {
        pollSCM('H/2 * * * *')
    }
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from Git...'
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building the project...'
                bat 'echo Build completed successfully'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'echo All tests passed'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                bat 'echo Deployment successful'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
