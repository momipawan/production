pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        node(label: 'wcncscmjst02')
        sh 'echo "hello"'
      }
    }
  }
}