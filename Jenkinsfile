pipeline {
 
    agent any

    stages {
 
        stage('checkout verification') {

	   steps {

              echo 'Welcome to jenkins Pipeline'
	      echo 'Building DOcker Image...'
              sh 'pwd'
              sh 'ls -l'
            
	  }
       stage('Build Docker Image') {
	  
 	   steps {
   		
	    sh 'docker build -t myjenkinswebsite:v1 .'
        	}
	} 
    
       stage('DOcekr image tag') {

	   steps {
          
            sh 'docker tag myjenkinswebsite:v1 lakareshital/myjenkinswebsite:v1'
        	}
	}
       }
    }
}
