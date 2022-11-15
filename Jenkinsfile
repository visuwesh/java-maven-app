pipeline {
	agent {
		label 'master'
	}
	tools {
        maven 'm1' 
    }
	stages {
		stage('Build') {
			steps {
				sh 'mvn -B -DskipTests clean install'
			}
		}
		stage('Test') {
			steps {
				sh 'mvn test'
			}
			post {
				always {
					jun 'target/surefire-reports/*.xml'
				}
			}
		}
		
	}
}
