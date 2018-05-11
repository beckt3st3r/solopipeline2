pipeline {
  agent any
  stages {
    stage('error') {
      environment {
        DEVICE = 'COOKIE'
      }
      steps {
        sh './build/prebuild.sh'
      }
    }
  }
}