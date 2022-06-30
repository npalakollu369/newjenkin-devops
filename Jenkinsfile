pipeline{
	agent any
	//agent {docker{image 'maven:3.6.3'}}
	stages{
		stage('Build'){
			steps{
				//sh 'mvn --version'
				echo "build"
				echo "path - $PATH"
				echo "BUILD NUMBER - $env.BUILD_NUMBER"
				echo "BUILD ID - $env.BUILD_ID"
				echo "JOB NAME - $end.JOB_NAME"
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