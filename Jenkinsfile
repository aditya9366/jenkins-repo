
pipeline {
	agent any
	stages {
		stage(planning) {
			node {
				def remote = [:]
        			remote.name = 'Terraform-server'
        			remote.host = '192.168.0.10'
        			remote.user = 'iac'
        			remote.password = 'iac'
        			remote.allowAnyHosts = true
			     }
			steps {
				sh 'pwd'
			}
			
			}
	}
	
}
		
		
			



			
		

	
