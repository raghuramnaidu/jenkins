pipeline {
    agent any

	tools {
		maven 'C:\opt\apache-maven-3.6.1'
	}

//	environment {
//		M2_INSTALL = "/home/gamut/Distros/apache-maven-3.6.0/bin/mvn"
//	}

    stages {
		stage('Clone-Repo') {
			steps {
				checkout scm
			}
		}
		stage('Build') {
	    	steps {
				 'mvn install -DskipTests'
			}
	    }
		stage('Unit Tests') {
			steps {
				 'mvn surefire:test'
			}
		}
		stage('Deployment') {
	    	steps {
				echo 'deployment'
	    	}
		}
    }
}
