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
*/

//Scripted//
node {
  docker.image('node:7-alpine').inside {
    stage('Check') {
     sh 'node --version' 
    }
  }
}
