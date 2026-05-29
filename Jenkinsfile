pipeline {
    agent any
    
    triggers {
        pollSCM('H/2 * * * *')
    }
    
    stages {
        stage('Checkout') {
            steps {
                echo ' Checking out code...'
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo ' Building project...'
                sh 'echo "Build successful"'
            }
        }
        stage('Test') {
            steps {
                echo ' Running tests...'
                sh 'echo "Tests passed"'
            }
        }
        stage('Deploy') {
            steps {
                echo ' Deploying...'
                sh 'echo "Deployment done"'
            }
        post {
        success {
            echo 'Pipeline executed successfully! - Updated Jenkinsfile'
        }
        failure {
            echo 'Pipeline failed!'
        }
        }
    }
}
