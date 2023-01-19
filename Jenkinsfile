pipeline {
	agent any
	// agent { docker { image 'node:14.17.6'} }
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('Checkout') {
			steps {
				sh 'mvn --version'
				sh 'docker version'
				echo "Build"
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "JOB_NAME - $env.JOB_NAME"
				}
			}
		stage('Compile') {
			steps {
				sh "mvn clean compile"
				}
			}
		stage('Test') {
			steps {
				sh "mvn test"
				}
			}
		stage('Int Test') {
			steps {
				sh "mvn failsafe:integration-test failsafe:verify"
				}
			}
		} 
		post {
			always {
				echo 'Im awesome'
			}
			success {
				echo 'I succedeed'
			}
			failure {
				echo 'I fail'
			}
		}
}
