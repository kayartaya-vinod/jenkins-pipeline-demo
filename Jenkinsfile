pipeline {
  agent any
  
  stages {
    stage('unit test'){
      steps{
        sh 'mvn clean test'
      }
    }
  
    stage('build'){
      steps {
        // expects mvn to be in OS PATH
        sh 'mvn -DskipTests=true package'
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
