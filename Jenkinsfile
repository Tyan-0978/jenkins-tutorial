/* Requires the Docker Pipeline plugin */
pipeline {
    agent any
    stages {
        stage('build') {
            environment {
                message = "building ..."
            }
            parameters {
                string(name: 'greet', defaultValue: 'Hello', description: '')
            }
            steps {
                echo "${env.message}"
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                echo $params.greet world
                sh "ls /"
            }
        }
    }
}
