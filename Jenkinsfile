/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'python:3.12-slim' } }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
}
