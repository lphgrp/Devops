pipeline {
	agent any
	stages {
		stage ("--Clean Project---") {
			step {
				bat "mvn clean"
			}
		}
		stage ("--Create WarFile---") {
			step {
				bat "mvn package"
			}
		}
		stage ("--Deploy WarFile---") {
			step {
				bat "copy taget\\MavenWeb.war D:\\LPH_Learning\\Installed_Soft\\Tomcat_Jenkins\\webapps\\"
			}
		}
	}
}