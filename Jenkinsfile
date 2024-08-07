pipeline{
	agent any
	stages{
		stage("Pull Latest Image"){
			steps{
				sh "docker pull mangeshkashid/mangesh-docker"
				}
			}
		stage("Start Grid"){
			steps{
				sh "docker-compose up -d selenium-hub chrome chrome1 chrome2 firefox"
				}
			}
		stage("Run Test"){
			steps{				
				sh "docker-compose up search-module"
				}
			}
		}
	post{
		always{
			archiveArtifacts artifacts: 'output/**'
			bat "docker-compose down"
		}
	}
}
