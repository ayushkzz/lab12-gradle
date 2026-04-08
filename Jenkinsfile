pipeline {
    agent any

    tools {
        jdk 'JDK17'
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ayushkzz/lab12-gradle.git'
            }
        }
        stage('Build & Test') {
            steps {
                sh './gradlew clean test'
            }
        }
    }
    post {
        always {
            junit '**/build/test-results/test/*.xml'
        }
    }
}
