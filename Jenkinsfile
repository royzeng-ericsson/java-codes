pipeline {
  agent {
    docker {
      image 'maven:latest'
    }
    
  }
  stages {
    stage('Test') {
      environment {
        CI = 'true'
      }
      steps {
        sh 'mvn clean test'
      }
    }
  }
}