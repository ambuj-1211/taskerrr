pipeline {
    agent {
        docker {
            // Use the Docker image with Node.js 14
            image 'node:14'
            args '-p 3000:3000'
            // Set the working directory to /app inside the container
            // dir '/app'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                // Install project dependencies
                sh 'npm install'
            }
        }
        // stage('Test') {
        //     steps {
        //         // Execute your test script
        //         sh './jenkins/scripts/test.sh'
        //     }
        // }
        // stage('Deliver') {
        //     steps {
        //         // Run your delivery script
        //         sh './jenkins/scripts/deliver.sh'
        //         // Prompt for user input
        //         input message: 'Finished using the web site? (Click "Proceed" to continue)'
        //         // Run cleanup script
        //         sh './jenkins/scripts/kill.sh'
        //     }
        // }
    }
}
