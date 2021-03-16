pipeline {
    agent any 
    stages {
        stage('Build Image') { 
            steps {
                echo 'Build docker image in local docker library...'
                sh './gradlew clean assemble'
            }
        }
        stage('Upload Image to Registry') { 
            steps {
                echo 'Push image to Harbor...'
                
            }
        }
        stage('Deploy to TKG Cluster') { 
            steps {
                echo 'Deploy application to TKG via TMC...'
                
            }
        }
        stage('Cleanup') { 
            steps {
                echo 'Remove local images and tags...'
                sh 'docker image rm tkgi-spring-music-pipeline:1.0'
                sh 'docker image rm savmas22/tkgi-spring-music-pipeline:${BUILD_NUMBER}'
                sh 'docker image rm savmas22/tkgi-spring-music-pipeline:latest'
            }
        }
    }
}
