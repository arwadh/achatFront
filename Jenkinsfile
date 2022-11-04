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
 
     
    stage('Build') {
      steps {
      
        sh "npm install"
     
      }
    }  
    
            
    stage('Test') {
      steps {
          sh "npm run build --prod"
      }
    }
  }
}
