pipeline {
    agent {
        label '1c-node'
    }
    post {
        always {
            bat "echo always"
        }
        failure {
            bat "echo failure"
        }
        success {
             bat "echo success"
        }
    }
    stages {
        stage('Example') {
            steps {
                bat "echo Hello world!"
            }
        }
    }
}