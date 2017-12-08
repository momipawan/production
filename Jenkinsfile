pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'This stage will be executed first.'
            }
        }
        stage('Sonar-Qube') {
            steps {
                echo "executing"
            }
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
            stage('Deploy') {
                steps {
                    echo "deploying to servers"
                }
                
            }
            
            
        }
        
        
    }
}
