pipeline {
    agent any
    environment {
        DOCKERHUB_CREDENTIALS = credentials('DockerHub')
    }

    tools {
        nodejs 'node_18.16.0'
    }

    stages {
        stage("Build") {
            steps {
                sh 'node --version'
                sh 'echo build section'
            }
        }
        
        
    }
    
}