pipeline {
	agent { label 'Ansible-server' }
        tools { 
        maven 'maven-3.6.3'
	
         
    }
	stages {
		stage('---clean---'){
			steps {
			
				sh "mvn clean"
			}
		}
		stage('---test---') {
			steps {
				
				sh "mvn test"
			}
		}
		stage('---package---'){
			steps {
				
				sh "mvn package"
			}
		}
		stage('Ansible Deploy') {
             
                        steps {
                 
              
                           
               sh 'ansible-playbook /ansible/deploy_tomcat-new.yml'
               
            }
	    }
	
	}
}
