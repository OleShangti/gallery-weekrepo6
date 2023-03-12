pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Git') {
      steps {
        git 'https://github.com/OleShangti/gallery-weekrepo6', branch: 'master'
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

    stage('Deploy to render') {
      steps {
        curl -d POST 'https://api.render.com/deploy/srv-cg5jrlkeoogsv97ov4og?key=9ANeAmDrGWs'
         sh '<<Deploy>>'
      }
    } 
    
    stage('END') {
      steps {
        echo 'Build has run Successfuly'
      }
    }
  }
}