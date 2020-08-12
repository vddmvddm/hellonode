pipeline {
  agent any
  tools {nodejs "nodejs"}
  stages {
    stage ('Clone repository') {
      steps {
        sh 'sudo cd /home/ansible/'
        sh 'ansible-playbook -i inventory hello_git_clone.yml -u ansible --private-key=/home/ansible/.ssh/id_rsa --tags clone'
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
