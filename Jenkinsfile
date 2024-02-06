pipeline {
    agent any {
        node {
            label 'agent-1'
        }
    }
    environment {
        GREETING = 'Hello Welcome to Jenkins!'
    }
    // build
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                    echo 'Here I wrote Shell Script'
                    env
                """
            }
        }
    }
    // post build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure {
            echo 'This will run when the pipeline fails, Generally runs to send alerts!'
        }
        success{
            echo 'This will run when the pipeline successes, Generally runs to send alerts!'
        }
    }
}