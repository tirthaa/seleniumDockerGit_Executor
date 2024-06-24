<<<<<<< HEAD
		pipeline{
			agent any
			stages{
					stage("Pull Latest Image"){
						steps{
								bat "docker pull mangeshkashid/mangesh-docker"
							 }
						}
					stage("Start Grid"){
						steps{
								bat "docker-compose up -d hub chrome firefox"
							 }
						}
					stage("Run Test"){
						steps{
								bat "docker-compose up search-module"
							 }					
						}
				  }
			post{
					always{
							archiveArtifacts artifacts: 'output/**'
							bat "docker-compose down"					
						  }			
				}		
=======
		pipeline{
			agent any
			stages{
					stage("Pull Latest Image"){
						steps{
								bat "docker pull mangeshkashid/mangesh-docker"
							 }
						}
					stage("Start Grid"){
						steps{
								bat "docker-compose up -d hub chrome firefox"
							 }
						}
					stage("Run Test"){
						steps{
								bat "docker-compose up search-module"
							 }					
						}
				  }
			post{
					always{
							archiveArtifacts artifacts: 'output/**'
							bat "docker-compose down"					
						  }			
				}		
>>>>>>> 3363c1ef8f421b183c86c92204984f1d83842dc2
			}