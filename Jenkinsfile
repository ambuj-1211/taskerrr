pipeline {
    agent {
        docker {
            // Use the Docker image with Node.js 14
            image 'node:14'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Install Docker') {
            steps {
                sh 'curl -fsSL https://get.docker.com -o get-docker.sh'
                sh 'sh get-docker.sh'
            }
        }
        stage('Build') {
            steps {
                // Install project dependencies
                sh 'npm install'
            }
        }
    }
}
