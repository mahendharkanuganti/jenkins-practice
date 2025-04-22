pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo this is build phase'
            }
        }
        stage('test') {
            steps {
                sh 'echo this is test phase'
            }
        }
        stage('deploy') {
            steps {
                sh 'echo this is deploy state'
            }
        }
    }
    post {
        always {
            echo 'i will always run'
        }
    }
}