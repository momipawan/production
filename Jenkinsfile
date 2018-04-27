pipeline {
    agent {label 'WCNCSCMJST05'
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from GitHub.'
            }
        }
        
        stage('Build') {
          parallel {
                stage('UnitTesting') {
                     steps {
                        echo "It is successfully completed"
                    }
                }
                
              
              
            }
        }
        
        stage('Upload-To-Nexus') {
            steps {
              echo 'uploading files to the Nexus repo'  
            }
        }
            stage('Approval') {
                parallel {
                  stage('Approval') {
                     steps {
                    echo "Approval is Accepted by pawan"
                }
             }
             stage('Deploy') {
                   steps {
                        echo "Executing Deployment"
                    }
                }     
                    
            }    
           }
        
    }
}
