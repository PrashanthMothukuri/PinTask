pipeline {
	agent none
	stages {
		stage('Non-Parallel Stage') {
			agent {
					label "any"
					}
			steps {
					echo "This stage will be executed first !!";
			}
		}
		
		stage('Run Tests') {
			parallel {
				stage('Test on windows') { 
					agent {
						label "any"
					}
					steps {
							echo "Task1 on Agent ";
					}
				}
		
				stage('Test on Master') {
					agent {
						label "any"
					}
					steps {
						echo "Task1 on Master";
					}
				}		
			}
		
		}	
	}
}
