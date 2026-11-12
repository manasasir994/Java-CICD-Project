
pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking Java project'
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling Java code'
                bat 'mvn clean compile'
            }
        }

        stage('Test') {
            steps {
                echo 'Running test cases'
                bat 'mvn test'
            }
        }

        stage('Package') {
            steps {
                echo 'Creating JAR file'
                bat 'mvn package'
            }
        }

        stage('Success') {
            steps {
                echo 'Java CI/CD Project Completed Successfully!'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESSFUL - GREEN'
        }

        failure {
            echo 'BUILD FAILED - RED'
        }
    }
}
