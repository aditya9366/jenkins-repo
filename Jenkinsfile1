
pipeline {
	agent any
	stages {
		stage(planning) {
			steps {
			  script {
				def remote = [:]
        			remote.name = 'Terraform-server'
        			remote.host = '192.168.0.10'
        			remote.user = 'iac'
        			remote.password = 'iac'
        			remote.allowAnyHosts = true
				sshCommand remote: remote, command: "cd /home/iac/aws && terraform plan"
				}
			  }
		}
			
			
			
	}
	
}
		
		
			



			
		

	
