pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building the project..."
                bat 'echo Build completed successfully!'
            }
        }
    }

    stages {
        stage('Test') {
            steps {
                echo "Running tests..."
                bat 'echo Tests passed!'
            }
        }
    }

    stages {
        stage('Deploy') {
            steps {
                echo "Deploying the applications..."
                bat 'echo Deployment successful!'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}