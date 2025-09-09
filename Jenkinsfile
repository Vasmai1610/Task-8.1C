pipeline {
    agent any
    triggers {
        pollSCM('H/1 * * * *') // Poll GitHub every minute
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Stage 1: Checkout latest code from GitHub'
                git branch: 'main', url: 'https://github.com/Vasmai1610/Task-8.1C.git'
            }
        }
        stage('Build') {
            steps { echo 'Stage 2: Build the project'; bat 'echo "Building project..."' }
        }
        stage('Code Quality Check') {
            steps { echo 'Stage 3: Run code quality analysis'; bat 'echo "Checking code quality..."' }
        }
        stage('Unit Testing') {
            steps { echo 'Stage 4: Run unit tests'; bat 'echo "Executing unit tests..."' }
        }
        stage('Integration Testing') {
            steps { echo 'Stage 5: Run integration tests'; bat 'echo "Executing integration tests..."' }
        }
        stage('Deployment to Staging') {
            steps { echo 'Stage 6: Deploy to staging environment'; bat 'echo "Deploying to staging..."' }
        }
        stage('Notification') {
            steps { echo 'Stage 7: Send notification to team'; bat 'echo "Sending notification...."' }
        }
    }
}
 
 