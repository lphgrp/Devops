pipeline {
	agent any
	stages {
		stage ("--Clean Project---") {
			steps {
				bat "mvn clean"
			}
		}
		stage ("----Code Coverage---")
		{
		steps {
				withSonarQubeEnv('Sonar_Analysis') {
				  bat "D:\\InstallSoft\\sonar-scanner-4.2.0.1873-windows\\bin\\sonar-scanner"
				}
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