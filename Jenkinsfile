pipeline {
    agent any

    stages {
        stage('Stage 1: Build') {
            steps {
                echo 'Building the code using Maven'
            }
        }

        stage('Stage 2: Unit and Integration Tests') {
            steps {
                echo 'Running unit tests using JUnit and integration tests using Selenium'
            }
        }

        stage('Stage 3: Code Analysis') {
            steps {
                echo 'Performing code analysis using SonarQube'
            }
        }

        stage('Stage 4: Security Scan') {
            steps {
                echo 'Performing security scan using OWASP ZAP'
            }
        }

        stage('Stage 5: Deploy to Staging') {
            steps {
                echo 'Deploying the application to the staging server'
            }
        }

        stage('Stage 6: Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on the staging environment using Selenium'
            }
        }

        stage('Stage 7: Deploy to Production') {
            steps {
                echo 'Deploying the application to the production server'
            }
        }
    }

    post {
        success {
            mail to: 'subhashsainani4@gmail.com',
                 subject: "Jenkins Pipeline: ${currentBuild.fullDisplayName}",
                 body: "The pipeline has completed successfully."
        }
        failure {
            mail to: 'subhashsainani4@gmail.com',
                 subject: "Jenkins Pipeline: ${currentBuild.fullDisplayName}",
                 body: "The pipeline has failed."
        }
    }
}