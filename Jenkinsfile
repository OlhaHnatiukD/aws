pipeline {
	agent any
	stages {
stage('Download Resources') {
	steps {
		git 'https://github.com/OlhaHnatiukD/aws.git'
	}
	}
	stage ('Check ansible connectivity') {
	steps {
		sh 'ansible -m ping webservers  -e ansible_python_interpreter=/usr/bin/python2.7'
	}
	}
  stage ('Run-Playbook'){
  steps{
    sh 'ansible-playbook /etc/ansible/roles/common/tasks/main.yml  -e ansible_python_interpreter=/usr/bin/python2.7'
  }
  }
}
}
  
