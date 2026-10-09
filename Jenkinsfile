pipeline {
    agent any

    tools {
        jdk 'JAVA-17'
    }

    stages {
        stage('Verify Java') {
            steps {
                bat 'java -version'
                bat 'javac -version'
                bat 'echo JAVA_HOME=%JAVA_HOME%'

            }
        }
        stage('Build') {
            steps {
                echo "Java is ready for build"
            }
        }
    }
    post {
        success {
            echo 'JDK setup and verification successful!'
        }
        failure {
            echo 'JDK seetup ot verification failed'
        }
    }
}
