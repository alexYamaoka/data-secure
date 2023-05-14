pipeline {
    agent any
    environment {
        DOCKERHUB_CREDENTIALS = credentials('DockerHub')
    }

    tools {
        nodejs 'node_18.16.0'
    }
    stages {
        // stage("Build Docker Image") {
        //     steps {
        //         echo 'building stage'
        //         sh 'docker build -t data-secure-app-image:1.0.0-prod'
        //     }
        // }

        stage("Login to DockerHub") {
            steps {
                sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
            }
        }

        // stage("Push Image to DockerHub") {
        //     steps {
        //         sh 'docker push react-demo/data-secure-app-image:1.0.0-prod'
        //     }
        // }
    }
    post {
        always {
            sh 'docker logout'
        }
    }
}