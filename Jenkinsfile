

pipeline {
	agent any 
	
	stages {            
		def remote = [:]
            	remote.name = 'testPlugin'
            	remote.host = '192.168.0.10'
            	remote.user = 'iac'
            	remote.password = 'iac'
		stage('terraform-plan') {
			steps {
				sshCommand remote: remote, command: "cd /home/terraform/aws" 
			}
		
		}
		
		stage('terraform-apply') {
			steps {
				sh 'ssh iac@192.168.0.10'
				sh 'cd /home/terraform/aws'
				sh 'terraform apply -auto-approve'
			      }
		
	                                  }
	
}

}
