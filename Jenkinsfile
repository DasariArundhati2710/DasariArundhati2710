pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh './gradlew assemble'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './gradlew test'
                }
            }
        }
    }

    post {
        success {
            echo 'Build and tests passed.'
        }
        failure {
            echo 'Build or tests failed.'
        }
    }
}
