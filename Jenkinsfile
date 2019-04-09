pipeline{

     agent{ label'slave1' }

     tools{
          maven 'maven'
	  jdk 'java8'
     }

	stages{

           stage('get the code from git') {

                      steps{
	                git credentialsId: '977d77ae-3d3b-4681-b5fc-352c869d5aee', url: 'https://github.com/bharathkattamanchi/webapp.git'
	                  }
	
        	}
	
	   stage('buillding the source code'){
	
	             steps{
	
                	sh 'mvn clean install'
	                }
        	}
	
	
	   stage ('send mail') {
	
	           steps{
	               emailext body: 'test project script', subject: 'devops project test', to: 'khbharaths@gmail.com'
		   }
	  
	      }
	  
	  }
	
}
