pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
   stage('Checkout SCM') {
        git branch: 'product',
         url:'https://github.com/arwadh/achatFront.git'
       
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
  }
}