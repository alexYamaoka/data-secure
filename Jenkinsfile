pipeline {
    agent any
    environment {
        DOCKERHUB_CREDENTIALS = credentials('DockerHub')
    }

    tools {
        nodejs 'node_18.16.0'
    }
    stages {
        stage("Build Docker Image") {
            steps {
                echo 'building stage'
                
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