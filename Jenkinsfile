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
			agent any
			steps {
				withDockerRegistry([ credentialsId: "dockerHub", url: "" ]) {
					sh 'docker push ubuntu'
				}
			}
		}
	}
}
