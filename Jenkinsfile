pipeline {
	agent any
	stages {
		stage ("--Clean Project---") {
			steps {
				bat "mvn clean"
				bat "mvn sonar.sonar"
			}
		}
		stage ("--Create WarFile---") {
			steps {
				bat "mvn package"
			}
		}
		stage ("--Deploy WarFile---") {
			steps {
				bat "copy target\\MavenWeb.war D:\\LPH_Learning\\Installed_Soft\\Tomcat_Jenkins\\webapps\\"
			}
		}
	}
}