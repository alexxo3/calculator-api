pipeline{

	agent any
	
	stages {
	
			stage('Build Application') {
			
					steps {
					
						bat 'mvn clean install'
					
					}
				}
				
			stage('Deploy CloudHubs') {
			
				environment {
				
					ANYPOINT_CREDENTIALS = credentials('752a257b-cfe0-44c5-a2b1-38de1a545d9c')
				
				}
			
				steps {
				
					echo 'Deploying mule project due to the latest code commit…'
				
					echo 'Deploying to the configured environment….'
				
					bat 'mvn -X clean deploy -DmuleDeploy -Dmule.app.name=cloudhub2-cicd -Dusername=Alexo12 -Dpassword=Alex12345'
				
				}
		
		}
	}
} 