pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Testing') {
            paralell {
            stage("Unit Test") {
            steps {
                echo 'Testing..'
            }
            }
              stage("Functional Tests") {
					steps {
						echo 'functional testing has been done'
					}
              } 
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
