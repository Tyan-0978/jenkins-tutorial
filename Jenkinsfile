/* Requires the Docker Pipeline plugin */
pipeline {
    agent any
    stages {
        stage('build') {
            environment {
                message = "building ..."
            }
            steps {
                echo ${env.message}
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                sh "ls"
            }
        }
    }
}
