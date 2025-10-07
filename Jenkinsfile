pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                bat 'javac Main.java'   // Windows command
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'java Main'         // Windows command
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
