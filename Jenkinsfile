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
        sh 'mvn -DskipTests package'
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

    post {
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
  }
}
