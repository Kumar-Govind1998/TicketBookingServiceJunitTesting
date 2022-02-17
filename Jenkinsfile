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
		      stage('Deploy') {
                            steps {
                                deploy adapters: [tomcat9(credentialsId: '7aeb140c-c542-4ed9-8a91-bfde64538c62', path: '', url: 'http://3.110.176.91:8090/')], contextPath: null, war: '**/*.war'   
                            }
                         }
		      
	          }
     }
