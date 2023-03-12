pipeline {
  agent any
    
  tools {nodejs "null"}
    
  stages {
        
    stage('Git') {
      steps {
        git 'https://github.com/OleShangti/gallery-weekrepo6'
      }
    }
     
    stage('Build') {
      steps {
        sh 'npm install'
         sh '<<Build Command>>'
      }
    }  

     stage('Test') {
      steps {
        sh 'node test'
      }
    }
  
    stage('END') {
      steps {
        echo 'Build has run Successfuly'
      }
    }
  }
}