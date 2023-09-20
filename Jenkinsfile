pipeline {
    agent {
        docker {
            // Use the Docker image with Node.js 14
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                // Install project dependencies
                sh 'npm install'
            }
        }
    }
}
