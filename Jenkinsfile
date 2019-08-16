pipeline {
	agent any
	stages {
	stage ('Check ansible connectivity') {
	steps {
		sh 'ansible -m ping webservers  -e ansible_python_interpreter=/usr/bin/python2.7'
	}
	}
  stage ('Run-Playbook'){
  steps{
    ansiblePlaybook credentialsId: 'aws1', inventory: 'hosts', playbook: '/etc/ansible/roles/common/tasks/main.yml'
	  ansibleVault(action: 'encrypt', input: '/etc/ansible/roles/common/credent.yml', vaultCredentialsId: 'ansible_vault_credentials')
	   }
  }
}
}
  
