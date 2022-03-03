pipeline {
  agent any
  options {
    buildDiscarder(logRotator(numToKeepStr: '2')) 
    disableConcurrentBuilds()
  }
  triggers {
        pollSCM('* * * * *')
   }
  
  stages {
  
    stage('Stage1') {
      steps { 
        sh 'echo Stag1'
      }
    }
    
    stage('Printfile') {
      steps {
        sh 'cat abc.txt'
      }
    }
    
    stage('Stage2') {
      steps { 
        sh 'echo Stag2'
      }
    }
    
  }
}
