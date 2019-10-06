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
        stage('terraform apply') {
				sshCommand remote: remote, command: "cd /home/iac/aws && terraform apply -auto-approve"
				}
}

node {
	stage ('test') {
		sh 'ls'
	}
}



			
		

	
