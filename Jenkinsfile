pipeline {
    agent any
    
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build("sher4win/docker-images-via-jenkins")
                }
            }
        }
        
        stage('Run Docker Container') {
            steps {
                script {
                    dockerImage.run('-d -p 7070:8080')
                }
            }
        }
    }
}
