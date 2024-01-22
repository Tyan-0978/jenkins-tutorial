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
            }
        }
        stage('run') {
            steps {
                echo 'Run stage'
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
