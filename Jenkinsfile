pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                // Call your build script here
                sh './build_script.sh'  // Adjust as necessary
            }
        }
        stage('Test') {
            steps {
                // Run tests if applicable
                sh './run_tests.sh'  // Adjust as necessary
            }
        }
        stage('Deploy') {
            steps {
                // Deploy your application
                sh './deploy_script.sh'  // Adjust as necessary
            }
        }
    }
    post {
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
