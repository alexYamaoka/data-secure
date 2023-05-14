pipeline {
    agent any

    tools {
        nodejs 'node_18.16.0'
    }
    stages {
        stage("Build") {
            steps {
                echo 'building stage'
                sh 'node --version'
            }
        }

        stage("Test") {
            steps {
                echo 'testing stage'
            }
        }

        stage("Deploy") {
            steps {
                echo 'deploying stage'
            }
        }
    }
}