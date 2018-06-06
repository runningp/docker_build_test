pipeline {
	agent none
	stages {
		stage('Build') {
			agent any
			steps {
				sh 'cd src .'
				sh 'docker build -f "Dockerfile" -t ubuntu .'
			}
		}
	}
}