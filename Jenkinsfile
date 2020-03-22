pipeline {
  agent {
    docker {
      image 'node/node:lts-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        sh 'npm test'
      }
    }

  }
  environment {
    CI = 'true'
  }
}