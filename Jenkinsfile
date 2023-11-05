pipeline {
	agent any 
	
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh '/home/abhilash/Documents/DevOps/tar/apache-tomcat-9.0.82/bin/mvn install'
	                 }}
		stage('Deployment'){
		   steps {
		sh 'cp target/grras2.war /home/abhilash/Documents/DevOps/tar/apache-tomcat-9.0.82/webapps'
			}}	
}}
