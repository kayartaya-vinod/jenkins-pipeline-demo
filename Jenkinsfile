pipeline {
  agent any
  
  stages {
    stage('build'){
      steps {
        // expects mvn to be in OS PATH
        sh 'mvn clean package'
      }
    }
    
    
    stage('test'){
      steps {
        echo 'Testing...' 
      }
    }
    
    
    stage('deploy'){
      steps {
        echo 'Deploying...' 
      }
    }
  }
}
