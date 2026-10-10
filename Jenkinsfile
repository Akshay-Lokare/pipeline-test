pipeline {
    agent any

    parameters {
        choice {
            name: "Environment",
            choices: [ 'DEV', 'TEST', 'PROD' ],
            description: "Select deployment environment",
        }
    }

    stages {
        stage("Build") {
            steps {
                bat 'echo Building app'
            }
        }
        stage("Test") {
            steps {
                bat 'echo Building app'
            }
        }
        stage("Deploy to DEV") {
            when {
                expression {
                    params.Environment == 'DEV'
                }
            }
            steps {
                bat 'echo Deploying to DEV'
            }
        }
        stage("Deploy to TEST") {
            when {
                expression {
                    params.Environment == 'TEST'
                }
            }
            steps {
                bat 'echo Deploying to TEST'
            }
        }
        stage("Deploy to PROD") {
            when {
                expression {
                    params.Environment == 'PROD'
                }
            }
            steps {
                bat 'echo Deploying to PROD'
            }
        }

    }

}