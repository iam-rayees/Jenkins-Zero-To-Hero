pipeline {
  agent none
  stages {
    stage('Checkout') {
        steps {
            //Checkout the code from your Github Repository 
            git ''
          
        }  
  
    }
    stage('Front-end') {
      agent {
        docker { image 'node:16-alpine' }
      }
      steps {
        sh 'node --version'
      }
    }
  }
}
