pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repo...'
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
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-node-app .'
            }
        }
        stage('Deploy') {
            steps {
                sh '''
                    docker stop my-node-app || true
                    docker rm my-node-app || true
                    docker run -d --name my-node-app -p 3000:3000 my-node-app
                '''
            }
        }
    }
    post {
        success { echo '✅ Build Passed!' }
        failure { echo '❌ Build Failed!' }
    }
}    
