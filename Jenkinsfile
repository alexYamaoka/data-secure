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

        stage("Login to DockerHub") {
            steps {
                echo 'login to dockerhub stage'
            }
        }

        
    }
   
}