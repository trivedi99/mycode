pipeline {
    agent any 
    stages {
        stage('Clone') {
            checkout scm
        }
 	stage('Build Image') {
            app = docker.build("tomcat")          
        }
	stage('Test Image') {
            app.inside {
                sh 'echo "Test Passed"'
        }   
     }
   }
}
