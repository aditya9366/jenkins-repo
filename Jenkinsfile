pipeline {
	agent any 
	
	stages {
		stage('terraform-plan') {
			steps {
				script 
				  {
    					sh """ssh iac@192.168.0.10 <<-EOF 
    					cd /home/terraform/aws
					terraform plan
    					exit
    					EOF"""
				  }
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
