/* pipeline {
  agent {
  docker { image 'node:7-alpine' }
  }
  stages{
    stage('Test'){
      steps {
        sh 'node --version'
      }
    }
  }
}


//Scripted //
node {
  docker.image('node:7-alpine').inside {
    stage('Check') {
     sh 'node --version' 
    }
  }
}
*/


pipeline {
 agent none
  
  stages {
    stage('front-end'){
      agent {
        docker {image 'maven:3-alpine'} 
      }
          steps {
            sh 'mvn --version' 
            sh 'hostname'
          }
      }
    
    stage('Back-end'){
      agent {
        docker { image 'node:7-alpine'}
       }
      steps {
       sh 'node --version' 
        sh 'hostname'
      }
    }
    }
  }
