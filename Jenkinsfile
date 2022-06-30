pipeline{
	agent any
	//agent {docker{image 'maven:3.6.3'}}
	environment{
		dockerhome= tool 'myDocker'
		mavenhome= tool 'myMaven'
		PATH= "$dockerhome/bin:$mavenhome/bin:$PATH"
	}
	stages{
		stage('Checkout'){
			steps{
				sh 'mvn --version'
				sh 'docker version'
				//echo "build"
				
			}
		}
		stage('compile'){
			steps{
				sh 'mvn clean compile'
			}
		}
		stage('Test'){
			steps{
				sh 'mvn test'
			}
		}
		stage('Integration Test'){
			steps{
				sh 'mvn failsafe:integration-test failsafe:verify'
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