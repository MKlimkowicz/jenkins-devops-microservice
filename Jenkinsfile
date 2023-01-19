pipeline {
	// agent any
	agent { docker { image 'node:14.17.6'} }
	stages{
		stage('Build') {
			steps {
				sh 'node --version'
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
				echo 'I fail'
			}
		}
}
