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
                bat "chcp 65001\n vrunner init-dev --v8version 8.3.27.1964 --dt C:\\1c\\dt\\20250511_2103.dt --src .\\src\\ cf --db-user Администратор --db-pwd 1215"
                // bat "echo Hello world!"
            }
        }
    }
}