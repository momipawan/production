pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'This Build will be executed first.'
            }
        }
        stage('Unit-Testing') {
            parallel {
                stage('Functional-testing') {
                    steps {
                        echo "Success"
                    }
                }
                stage('Code-Coverage Report') {
                    steps {
                        echo "Executing Code Coverage report"
                    }
                }
            }
            stage('Upload Zip To Nexus'){
              echo "uploading"
           }  
        } 
               
   }
  
}
