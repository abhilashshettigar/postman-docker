pipeline {
   agent {
        docker {
            image 'node:10-alpine'
        }
    }
   environment {
        CI = 'true'
        HOME="."
    }
  stages {
    stage('Install Dependecis') {
      steps {
        sh 'npm install && npm install http-server'
      }
    }
    stage('Test') {
      steps {
        sh 'npm run deploy'
          publishHTML (target: [
      allowMissing: false,
      alwaysLinkToLastBuild: false,
      keepAll: true,
      reportFiles: 'index.html',
    ])
      }
    }
  }
}