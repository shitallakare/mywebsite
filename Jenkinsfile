pipeline {
 
    agent any

    stages {
 
        stage('BUild Docker image') {

	   steps {

              echo 'Welcome to jenkins Pipeline'
	      echo 'Building DOcker Image...'
              sh 'pwd'
              sh 'ls -l'
              sh 'docker build -t myjenkinswebsite:v1 .'

	  }

       }
    }
}
