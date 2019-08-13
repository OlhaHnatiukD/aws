pipeline {
<<<<<<< HEAD
	agent any
	stages {
	stage ('Check ansible connectivity') {
	steps {
		sh 'ansible -m ping  webservers '
	}
	}
=======
        agent any
        stages {
        stage ('Check ansible connectivity') {
        steps {
                sh 'ansible -m ping  webservers  -e ansible_python_interpreter=/usr/bin/python2.7 '
        }
        }
>>>>>>> 836dc8b42879324e341cefbb3a2476a64105bbc5
  stage ('Run-Playbook'){
  steps{
    sh 'ansible-playbook  roles/jenk/tasks/main.yml -e ansible_python_interpreter=/usr/bin/python2.7'
  }
  }
}
}
<<<<<<< HEAD

=======
>>>>>>> 836dc8b42879324e341cefbb3a2476a64105bbc5
