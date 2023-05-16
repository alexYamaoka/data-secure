pipeline {
    agent any
    //  agent {
    //     label 'jenkins_agent'
    // }

    environment {
        DOCKERHUB_CREDENTIALS = credentials('dockerhub')
    }

    // tools {
    //     nodejs 'node_18.16.0'
    // }
    
    stages {
        stage("Build Docker Image") {
            steps {
                echo 'building stage'
                sh 'docker build -t ryamaoka/react-docker-app:1.0.0-prod .'
                sh 'docker ps'
                sh 'docker images'
            }
        }

        stage("Login to DockerHub") {
            steps {
                echo 'login to dockerhub stage'
                sh 'echo DOCKERHUB_CREDENTIALS_USR'
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
            }
        }

        stage("Push Image to DockerHub") {
            steps {
                echo 'push image to dockerhub stage'
                sh 'docker push ryamaoka/react-docker-app:1.0.0-prod'

            }
        }

        
    }
    post {
        always {
            sh 'docker logout'
        }
    }
}