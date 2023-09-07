pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'gcc hello.c -o hello'
                sh 'ls -la'
            }
        }
        stage('Test') {
            steps {
                sh './hello'
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: 'hello', fingerprint: true
        }
    }
}
