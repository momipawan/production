pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'This stage will be executed first.'
            }
        }
        stage('Testing') {
          parallel {
                stage('Unit-Testing') {
                     steps {
                        echo "It is successfully completed"
                    }
                }
                stage('Code-Coverage') {
                   steps {
                        echo "Reports is Generated"
                    }
                }
              
              
            }
        }
        
        stage('Upload-To-Nexus') {
            steps {
              echo 'uploading files to the Nexus repo'  
            }
        }
            stage('Deploy') {
                parallel {
                  stage('Deployment') {
                     steps {
                    echo "deploying to the servers"
                }
             }
             stage('Wait for Approval') {
                   steps {
                        echo "Build is waiting  for manager approval"
                    }
                }     
                    
            }    
           }
        
    }
}
