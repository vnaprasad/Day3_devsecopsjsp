pipeline {

agent any

tools {
	maven 'maven'

 }

stages {
	stage('checkcing maven installation'){
            steps {
			sh 'mvn -v'

		}
	}
	
	stage('security checking by trufflehog'){
		steps {
			sh 'docker run  --rm  gesellix/trufflehog --json  https://github.com/vnaprasad/Day3_devsecopsjsp.git  >mybugs.txt'
			sh 'cat mybugs.txt'
		
		
		 }
	
	
	
	}
	
	stage('build java project'){
		steps {
			sh 'mvn clean package'
		
		}
	
	}


 }

}
