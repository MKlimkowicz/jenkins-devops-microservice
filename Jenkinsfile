pipeline {
	// agent any
	agent { docker { image 'maven:3.6.3'} }
	stages{
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo "Build"
				}
			}
		stage('Test') {
			steps {
				echo "Test"
				}
			}
		stage('Int Test') {
			steps {
				echo "Int Test"
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
				echo 'I failed'
			}
		}
}
