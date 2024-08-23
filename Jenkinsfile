pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project using Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests with Selenium'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing code quality with SonarQube'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan with OWASP Dependency Check'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging server with AWS CLI'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging with Selenium'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production server AWS CLI'
            }
        }
    }

    post {
        success {
            emailext to: "azelmaava@gmail.com",
            subject: "Build Status Email - SUCCESS",
            body: "Build was successful!",
            attachLog: true
        }
        failure {
            emailext to: "azelmaava@gmail.com",
            subject: "Build Status Email - FAILURE",
            body: "Build was unsuccessful!",
            attachLog: true
        }
    }
}
