pipeline {
    agent any

    stages {
		stage('Clone-Repo') {
			steps {
				checkout scm
			}
		}
		stage('Build') {
	    	steps {
				 mvn install -DskipTests
			}
	    }
		stage('Unit Tests') {
			steps {
				 mvn surefire:test
			}
		}
		stage('Deployment') {
	    	steps {
			echo 'deployment'
	    			}
			}
		}
}
