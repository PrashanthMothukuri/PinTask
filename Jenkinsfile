pipeline {
	agent any
	stages {
		stage('compile') {
			steps {
					echo "compiled successfully !!";
			}
		}
		
		stage('JUnit') {
			steps {
					echo "JUnite passed successfully";
			}
		}
		
		stage('Quality-Gate') {
			steps {
					echo "SonarCube quality gate passed successfully";
			}
		}
		
		stage('Deploy') {
			steps {
					echo "Pass !!";
			}
		}
		
		
	}
	post {
		always {
				echo 'This will always Run'
		}
		success {
				echo 'This will run only if successful'
		}
		failure {
				echo 'This will run only if failed'
		}
		unstable {
				echo 'This will run only if the run was marked as unstable'
		}
		changed {
				echo 'This will run only if the state of the Pipeline has changed'
				echo 'For ex: if the Pipeline was previously failing but is now successful'
		}
	}
}
