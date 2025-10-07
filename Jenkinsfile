pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'javac Main.java'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'java Main'
            }
        }
        stage('Archive') {
            steps {
                echo 'Archiving artifacts...'
                archiveArtifacts artifacts: '*.class', fingerprint: true
            }
        }
    }
}
