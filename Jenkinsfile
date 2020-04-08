pipeline {
	agent any
	stages {
		stage ("--Clean Project---") {
			steps {
				bat "mvn clean"
			}
		}
		stage ("----Code Coverage---")
		steps {
		def scannerhome = tool 'SonarScanner';
				withSonarQubeEnv('Sonar_Qube') {
				  bat "${scannerHome}/bin/sonar-scanner"
				}
			}
		
		stage ("--Create WarFile---") {
			steps {
				bat "mvn package"
			}
		}
		stage ("--Deploy WarFile---") {
			steps {
				bat "copy target\\MavenWeb.war D:\\InstallSoft\\Devops\\"
			}
		}
	}
}