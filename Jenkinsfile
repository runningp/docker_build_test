pipeline {
	agent none
	stages {
		stage('Build') {
			agent any
			steps {
				sh 'docker build -f "Dockerfile" -t ubuntu .'
			}
		}
		stage('Push') {
			steps {
				withDockerRegistry([ credentialsId: "cnVubmluZ3A6NjU0MzIxIQ==", url: "" ]) {
					sh 'docker push ubuntu'
				}
			}
		}
	}
}