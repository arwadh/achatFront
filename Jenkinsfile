node {
    stage('Checkout SCM') {
        git branch: 'product', url:'https://github.com/arwadh/achatFront.git'
       
    }

    stage('NPM Install node modules') {
       
            sh 'npm install'
        
    }

    stage('Build') {
        sh 'npm run build:ssr '
    }

    stage('Deploy') {
        sh 'pm2 restart all '
    }



  
}