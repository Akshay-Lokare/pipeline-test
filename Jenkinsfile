pipeline {
    agent any

    stages {
        stage('Use Jenkins Java 17') {
            tools {
                jdk 'JAVA-17'
            }
            steps {
                echo "Using jenkins-managed file"
                bat 'java -version'
                bat 'javac -version'
                bat 'echo JAVA_HOME=%JAVA_HOME%'

            }
        }
        stage('Use Jenkins Java 21') {
            steps {
                echo "Using system-installed file"
                bat "C:\\Program Files\\Eclipse Adoptium\\jdk-21.0.12.101-hotspot\\bin\\java.exe"
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
        stage("Use Jenkins Java Again") {
            tools {
                jsd 'JAVA-17'
            }
            steps {
                bat 'java -version'
            }
        }
    }
}
