pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Code checked out!'
                checkout scm
            }
        }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }
    post {
        success { echo '✅ Build Passed!' }
        failure { echo '❌ Build Failed!' }
    }
}
