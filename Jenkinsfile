pipeline {
	agent any
	stages {
 
  		stage('SCM') {
			steps {
    				sh 'checkout scm'
  		}
}
 		 stage('SonarQube Analysis') {
			steps {
  	  			withSonarQubeEnv() {
      				sh './gradlew sonar'
    			}
  		}
	}
}
