pipeline{
	agent any
	stages{
		stage('Build'){
			steps{
				echo "build"
			}
		}
		stage('Test'){
			steps{
				echo "Test"
			}
		}
		stage('Integration Test'){
			steps{
				echo "Integration Test"
			}
		}
	}
	post{
		always{
			echo "I run always"
		}
		success{
			echo " I run when success"
		}
		failure{
			echo " I run on failure"
		}
	}
}