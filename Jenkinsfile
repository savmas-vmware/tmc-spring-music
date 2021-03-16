pipeline {
    agent any 
    stages {
        stage('Build Image') { 
            steps {
                echo 'Build docker image in local docker library...
            }
        }
        stage('Upload Image to Registry') { 
            steps {
                echo 'Push image to Harbor...'
            }
        }
        stage('Deploy to TMC Provisioned Cluster') { 
            steps {
                echo 'Deploy application to TMC Provisioned Cluster'
                
            }
        }
        stage('Cleanup') { 
            steps {
                echo 'Remove local images and tags...'
      
            }
        }
    }
}
