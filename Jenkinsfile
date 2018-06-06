pipeline {
	agent none
	stages {
		stage('Build') {
			agent any
			steps {
				sh 'docker build -f "src/Dockerfile" -t ubuntu .'
			}
		}
	}
}