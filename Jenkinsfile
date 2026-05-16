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
                bat "chcp 65001\n vrunner init-dev "
                // bat "echo Hello world!"
            }
        }
    }
}