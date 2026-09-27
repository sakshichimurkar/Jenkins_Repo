pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }

        stage('Test') {
            steps {
                withEnv(['PATH+NODE=/opt/homebrew/bin'])
                sh 'npm test'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline completed successfully.'
        }
        failure {
            echo 'CI Pipeline failed. Check the console output.'
        }
        always {
            echo 'Pipeline finished. This always runs.'
        }
    }
}


