pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                gcc hello.c -o hello
                ls -la
            }
        }
        stage('Test') {
            steps {
                sh './hello'
            }
        }
        }
