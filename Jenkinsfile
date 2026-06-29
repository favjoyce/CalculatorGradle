pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/favjoyce/CalculatorGradle', branch: 'main'
            }
        }

        stage('Compile') {
            steps {
                // Use the Windows Gradle wrapper to clean and compile
                bat 'gradlew.bat clean compileJava'
            }
        }

         stage('Unit Test') {
                    steps {
                        bat 'gradlew.bat test'
                    }
                }
    }
}