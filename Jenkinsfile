pipeline {
	agent any
	stages {
 
  		stage('SCM') {
			steps {
    				checkout scm
  		}
}
 		 stage('SonarQube Analysis') {
			steps {
  	  			withSonarQubeEnv() {
      				sh "./gradlew sonar"
    			}
  		}
	}
}
