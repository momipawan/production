pipeline {
    agent {label 'WCNCSCMJST05'
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from GitHub.'
            }
        }
        
        stage("Build") {
			parallel {
				stage("Unit Tests") {
					steps {
						echo 'done'
					}
				}
				stage("Functional Tests") {
					steps {
						echo 'java -version'
					}
				}
				stage("Integration Tests") {
					steps {
						echo 'java -version'
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
