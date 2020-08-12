pipeline {
  agent any
  tools {nodejs "nodejs"}
  stages {
    stage ('Clone repository') {
      steps {
        sh 'cd /home/ansible/'
        sh 'ansible-playbook -i inventory hello_git_clone.yml --tags clone'
      }
    }
    stage ('Install dependencies') {
      steps {
        sh 'cd /home/ansible/'
        sh 'ansible-playbook -i inventory hello_git_clone.yml --tags dependencies'
      }
    }
    stage ('Test') {
      steps {
        sh 'cd /home/ansible/'
        sh 'ansible-playbook -i inventory hello_git_clone.yml --tags test'
      }
    }
    stage ('Run') {
      steps {
        sh 'cd /home/ansible/'
        sh 'ansible-playbook -i inventory hello_git_clone.yml --tags run'
      }
    }
  }
}
