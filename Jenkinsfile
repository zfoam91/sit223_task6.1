pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests...'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing code quality...'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan...'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging server...'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production server...'
            }
        }
    }

    post {
        success {
            emailext (
                to: 'developer@example.com',
                subject: "Pipeline Successful: ${currentBuild.fullDisplayName}",
                body: "The pipeline has completed successfully.",
                attachLog: true
            )
        }
        failure {
            emailext (
                to: 'developer@example.com',
                subject: "Pipeline Failed: ${currentBuild.fullDisplayName}",
                body: "The pipeline has failed. Please check the logs.",
                attachLog: true
            )
        }
    }
}
