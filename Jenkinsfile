pipeline {

	agent any

	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			   sh '/home/shubham/DevOps/apache-maven-3.6.3/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			   sh 'sshpass -p "tux" scp target/LoginWebApp.war tux@172.17.0.2:/home/tux/apache-tomcat-8.5.65/webapps'
			}}
       		
	}
}
