@Library('lib') _

pipeline {
    agent any
    stages {
        stage('build') {
            environment {
                message = "building ..."
            }
            steps {
                echo "${env.message}"
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        stage('greet') {
            steps {
                echo "Hello"
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
