pipeline {
    agent any

    stages {
        stage('Use Jenkins Java 17') {
            tools {
                jdk 'JAVA-17'
            }
            steps {
                echo "Using Jenkins-managed Java 17"
                bat 'java -version'
                bat 'javac -version'
                bat 'echo JAVA_HOME=%JAVA_HOME%'
            }
        }

        stage('Use Jenkins Java 21') {
            steps {
                echo "Using system-installed Java 21"
                bat '"C:\\Program Files\\Eclipse Adoptium\\jdk-21.0.12.101-hotspot\\bin\\java.exe" -version'
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

        stage('Use Jenkins Java Again') {
            tools {
                jdk 'JAVA-17'
            }
            steps {
                bat 'java -version'
            }
        }
    }
}