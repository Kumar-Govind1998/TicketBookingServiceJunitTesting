     pipeline {
       agent any
              stages {
                   stage('Clone') {
                         steps {
                            git credentialsId: 'Github', url: 'https://github.com/Ijaz0059/welcometoskillrary.git'
                            }
                         }
                   stage('Build') {
                            steps {
                                sh "mvn clean install"   
                            }
                         }
		      stage('Deploy to Tomcat'){
			      steps{
                               sh "/var/lib/jenkins/workspace/newjob/webapp/target/webapp.war /usr/share/tomcat/webapps"
				    
				   }
		      }
                      
		      
	          }
     }
