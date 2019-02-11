pipeline {
  agent {
    image 'node:10-alpine'
  }
   environment {
        CI = 'true'
        HOME="."
    }
  stages {
    stage('Install Dependecis') {
      steps {
        sh 'npm install && npm install -g http-server'
      }
    }
    stage('Test') {
      steps {
        sh 'npm run deploy'
      }
    }
  }
}