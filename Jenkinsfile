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
	}
       stage('Build Docker Image') {
	  
 	   steps {
   	    echo 'Building docker image'	
	    sh 'docker build -t myjenkinswebsite:v1 .'
        	}
	} 
    
       stage('DOcekr image tag') {

	   steps {
            echo 'tagging docker image'
            sh 'docker tag myjenkinswebsite:v1 lakareshital/myjenkinswebsite:v1'
        	}
	}

 	stage('login to docker hub credentials') {
	 
	   steps {
          
	    withCredentials([usernamePassword(
             credentialsId: 'dockerhub',
             usernameVariable: 'DOCKER_USER',
   	     passwordVariable: 'DOCKER_PASS'
	   )]) {

	   
	     sh '''
		echo "$DOCKER_PASS" | docker login -u "$DOCKER_USER" --password-stdin
	      '''    
	        echo 'docker hub logged in succesfully'
	}

 
       }
    }
 }
}
