pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo this is build phase'
                echo "Hello ${params.PERSON}"
                echo "toggle ${params.TOGGLE}"
                echo "choice ${params.CHOICE}"
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