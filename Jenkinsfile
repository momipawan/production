pipeline {
    agent any
    stages {
        stage('Non-Parallel Stage') {
            steps {
                echo 'This stage will be executed first.'
            }
        }
       
            
            parallel {
                stage('Branch A') {
                   
                    steps {
                        echo "On Branch A"
                    }
                }
                stage('Branch B') {
                  
                    steps {
                        echo "On Branch B"
                    }
                }
            
        }
    }
}
