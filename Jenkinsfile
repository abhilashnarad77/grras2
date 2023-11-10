pipeline {
	agent any
	triggers {
  pollSCM '* * * * *'
}
parameters {
		choice(name: 'ENVIRONMENT', choices: ['QA','UAT'], description: 'Pick Environment value')
	}
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/abhilash/Documents/DevOps/tar/apache-maven-3.9.5/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/grras2.war /home/abhilash/Documents/DevOps/tar/apache-tomcat-9.0.82/webapps'
			}}	
}}
slackSend enCredentialId: 'dedf9f6c-d136-40d9-bf15-c67a2bf3b45c'
