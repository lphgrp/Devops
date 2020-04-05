pipeline {
	agent any
	stages {
		stage ("--Clean Project---") {
			steps {
				bat "mvn clean"
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