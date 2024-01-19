/* Requires the Docker Pipeline plugin */
pipeline {
    agent any
    parameters {
        string(name: 'greet', defaultValue: 'Hello', description: '')
    }
    stages {
        stage('build') {
            environment {
                message = "building ..."
            }
            steps {
                echo "${env.message}"
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                echo "${params.greet} world"
                echo "Test scan"
                sh "ls /"
            }
        }
        stage('run') {
            steps {
                python script.py
            }
        }
    }
}
