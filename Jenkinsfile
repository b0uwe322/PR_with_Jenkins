pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url:'https://github.com/b0uwe322/PR_with_Jenkins', branch: 'main'
            }
        }
        stage('Install') {
            steps {
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat 'pytest'
            }
        }
    }
}