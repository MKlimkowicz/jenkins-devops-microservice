pipeline {
	agent any
	stages{
		stage('Build') {
			steps {
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
		} post {
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
