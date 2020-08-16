pipeline {
  agent any
  tools {nodejs "node"}
  stages {
    stage ('Clone repository') {
      steps {
        sh 'ansible-playbook -i inventory hello_git_clone.yml --tags clone'
      }
    }
    stage ('Install dependencies') {
      steps {
        sh 'ansible-playbook -i inventory hello_git_clone.yml --tags dependencies'
      }
    }
    stage ('Test') {
      steps {
        sh 'ansible-playbook -i inventory hello_git_clone.yml --tags test'
      }
    }
    stage ('Run') {
      steps {
        sh 'ansible-playbook -i inventory hello_git_clone.yml --tags run'
      }
    }
  }
}
