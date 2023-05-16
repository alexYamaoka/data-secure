pipeline {
    agent any
    //  agent {
    //     label 'jenkins_agent'
    // }

    // environment {
    //     DOCKERHUB_CREDENTIALS = credentials('dockerhub')
    // }

    // tools {
    //     nodejs 'node_18.16.0'
    // }
    
    stages {
        stage("Build Docker Image") {
            steps {
                echo 'building stage'
                //sh 'docker build -t react-docker-app:1.0.0-prod .'
                //sh 'docker ps'
            }
        }

        stage("Login to DockerHub") {
            steps {
                echo 'login to dockerhub stage'
                //sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
            }
        }

        stage("Push Image to DockerHub") {
            steps {
                echo 'push image to dockerhub stage'
            }
        }

        
    }
    // post {
    //     always {
    //         sh 'docker logout'
    //     }
    // }
}