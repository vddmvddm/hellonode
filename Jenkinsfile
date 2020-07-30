pipeline {
  agent any
  stages {
    stage ('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
    stage ('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage ('Run') {
      steps {
        sh 'pm2 start app.js'
      }
    }
  }
}
