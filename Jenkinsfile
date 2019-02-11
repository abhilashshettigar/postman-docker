pipeline {
  agent {
    dockerfile true
  }
   environment {
        CI = 'true'
        HOME="."
    }
  stages {
    stage('test') {
      steps {
        echo 'test'
      }
    }
  }
}