pipeline {
  agent any
  tools {nodejs "nodejs"}
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
        sh 'node app.js'
      }
    }
  }
}
