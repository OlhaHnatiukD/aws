pipeline {
        agent any
        stages {
        stage ('Check ansible connectivity') {
        steps {
                sh 'ansible -m ping  webservers  -e ansible_python_interpreter=/usr/bin/python2.7 '
        }
        }
  stage ('Run-Playbook'){
  steps{
    sh 'ansible-playbook  roles/jenk/tasks/main.yml -e ansible_python_interpreter=/usr/bin/python2.7'
  }
  }
}
}
