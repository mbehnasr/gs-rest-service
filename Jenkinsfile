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
			steps {
      				sh './gradlew sonar   -Dsonar.projectKey=fuck   -Dsonar.host.url=http://172.17.0.3:9000   -Dsonar.login=sqp_b62bf4ad54646c2102cbf267d526d853bc875b35'
  		}
	}
}
}
