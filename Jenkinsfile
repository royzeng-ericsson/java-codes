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
    stage('Package') {
      steps {
        sh 'mvn package'
      }
    }
    stage('clean') {
      steps {
        sh 'mvn clean'
      }
    }
  }
}