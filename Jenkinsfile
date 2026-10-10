pipeline {
    agent any

    stages {
        stage("Show Parameters") {
            steps {
                echo "Select Environment: ${params.Environment}"
                echo "Run Tests: ${params.RunTests}"
            }
        }
        stage("Build") {
            steps {
                bat 'echo Building app'
            }
        }
        stage("Test") {
            steps {
                bat 'echo Testing app'
            }
        }
        stage("Deploy") {
            steps {
                bat 'echo Deploy app'
            }
        }
    }

}