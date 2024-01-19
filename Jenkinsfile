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
            }
        }
        stage('run') {
            steps {
                echo 'Run stage'
                echo $abc
            }
        }
    }
    post {
        always {
            echo 'End pipeline'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
