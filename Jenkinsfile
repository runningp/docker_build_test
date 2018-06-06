pipeline {
	agent none
	stages {
		stage('Build') {
			agent any
			steps {
				sh 'docker build -f "Dockerfile" -t ubuntu .'
			}
		}
	}
}