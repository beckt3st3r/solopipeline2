pipeline {
  agent any
  stages {
    stage('error') {
      environment {
        DEVICE = 'COOKIE'
      }
      steps {
        build 'Demo2Job1'
      }
    }
  }
}