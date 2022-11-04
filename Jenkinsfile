pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Git') {
      steps {
           echo ('Getting project from git');
          git branch: 'product',
         url:'https://github.com/arwadh/achatFront.git'
      }
    }
      stage('cache clean') {
      steps {
        sh 'npm cache clean --force'
         sh '<<Build Command>>'
      }
    } 
     
    stage('Build') {
      steps {
        sh 'npm i @angular-devkit/build-angular@12.0.5 --force'
        sh 'npm install'
         sh 'npm audit fix --force'
      }
    }  
    
            
    stage('Test') {
      steps {
        sh 'node test'
      }
    }
  }
}