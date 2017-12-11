pipeline {
    agent any
    stages {
        stage('Checkout-Source') {
            steps {
                echo 'Pulling code from GitHub.'
            }
        }
        stage('Build') {
            steps {
              echo 'Compiling the source code'  
            }
        }
        stage('SonarQube') {
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
            stage('Wait For Approval') {
                parallel {
                  stage('Approval') {
                     steps {
                    echo "Approval is Accepted by pAwan"
                }
             }
             stage('Deployment') {
                   steps {
                        echo "Executing Deployment"
                    }
                }     
                    
            }    
           }
        
    }
}
