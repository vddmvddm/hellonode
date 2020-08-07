pipeline {
  agent any
  tools {nodejs "nodejs"}
  stages {
    stage ('Clone repository') {
      steps {
        sh 'cd /var/lib/jenkins/ansible/'
        sh 'ansible-playbook -i inventory hello_git_clone.yml'
    }
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
