pipeline {
	agent any
	stages {
		stage("clone code"){
			steps{ 
			    git 'https://github.com/bijleengr/maven-web-application.git'
			    
			}
		}
		stage("build code") {
			steps{
				sh "mvn clean install"
			}
	}
	}
    
}
