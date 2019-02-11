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
        sh 'npm run deploy'
      }
    }
  }
}