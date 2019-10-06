node {
			def remote = [:]
            		remote.name = 'testPlugin'
            		remote.host = '192.168.0.10'
            		remote.user = 'iac'
            		remote.password = 'iac'
			remote.allowAnyHosts = true
			stage('terraform-plan') {
				sshCommand remote: remote, command: "cd /home/iac/aws && terraform plan"
				}
}
			
		
stage('terraform-apply') {
	steps {
		sh 'ssh iac@192.168.0.10'
		sh 'cd /home/terraform/aws'
		sh 'terraform apply -auto-approve'
		}
}
	
