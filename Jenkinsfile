pipeline {
  agent any
  stages {
    stage('Build1') {
      parallel {
        stage('error') {
          environment {
            DEVICE = 'COOKIE'
          }
          steps {
            sh './build/prebuild.sh'
          }
        }
        stage('Build2') {
          environment {
            DEVICE = 'dev2'
          }
          steps {
            build 'Demo2Job1'
          }
        }
      }
    }
  }
}