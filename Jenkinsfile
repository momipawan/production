pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'This Build will be executed first.'
            }
        }
        stage('Unit-Testing') {
            when {
                branch 'master'
            }
            parallel {
                stage('Functional-testing') {
                    steps {
                        echo "Success"
                    }
                
            }
          stage('Regression-testing') {
             steps {
                     echo "Success"
                    }
                
            }
                
                
            }
       
        } 
               
   }
  
}
