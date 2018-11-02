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
  checkout scm
  docker.image('node:7-alpine').inside {
    stage('Check') {
     sh 'node --version' 
          }
  }
}
*/

node {
    checkout scm

    def customImage = docker.build("my-image:test")

    customImage.inside {
        sh 'make test'
    }
}


/*pipeline {
 agent none
  
  stages {
    stage('front-end'){
      agent {
        docker {image 'maven:3-alpine'} 
      }
          steps {
            sh 'mvn --version' 
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
*/

