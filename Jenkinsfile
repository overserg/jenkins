pipeline {
    agent {
        label '1c-node'
    }
    post {
        always {
            allure commandline: 'allure-cli', includeProperties: false, jdk: '', resultPolicy: 'LEAVE_AS_IS', results: [[path: 'out/syntax-check/allure']]
            junit 'out/syntax-check/junit/junit.xml'
        }
        // failure {
        //     bat "echo failure"
        // }
        // success {
        //      bat "echo success"
        // }
    }
    stages {
        stage('Example') {
            steps {
                bat "chcp 65001\n vrunner init-dev "
                // bat "echo Hello world!"
            }
        }
        stage('Syntax-check') {
            steps {
                bat "chcp 65001\n vrunner syntax-check"
            }
        }
    }
}