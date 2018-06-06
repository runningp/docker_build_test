pipeline {
	agent none
	stages {
		stage('Build') {
			agent any
			steps {
				sh 'docker build -f "Dockerfile" -t runningp/test1 .'
			}
		}
		stage('Push') {
			agent any
			steps {
				withDockerRegistry([ credentialsId: "dockerHub", url: "" ]) {
					sh 'docker push runningp/test1'
				}
			}
		}
	}
}
