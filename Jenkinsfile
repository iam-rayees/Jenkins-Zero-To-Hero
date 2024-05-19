pipeline {
  agent none
  stages {
    stage('Checkout') {
        steps {
            //Checkout the code from your Github Repository 
            git 'https://github.com/iam-rayees/Jenkins-Zero-To-Hero.git'
          
        }  
    }
    stage('Build') {
      agent {
        docker { image '' }
      }
      steps {
        sh 'node --version'
      }
    }
  }
}
