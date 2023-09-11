pipeline {
	agent any
	stages {
/* 
  		stage('SCM') {
			steps {
    				sh 'checkout scm'
  		}
}
*/
 		 stage('SonarQube Analysis') {
			withSonarQubeEnv ('sast') {
			steps {

      				sh './gradlew sonar   -Dsonar.projectKey=sast   -Dsonar.host.url=http://172.17.0.3:9000   -Dsonar.login=sqp_91112e985bfdbef2251beeb00831a00c82c3f0a4'
  		}
			timeout(time: 2 , unit : 'MINUTES') {
				script {
					waitForQualityGate abortPipeline : true
}
}
	}
}
}
}
