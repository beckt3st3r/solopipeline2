pipeline {
  agent any
  stages {
    stage('PreBuild') {
      parallel {
        stage('Pre1') {
          environment {
            DEVICE = 'COOKIE'
          }
          steps {
            sh './build/prebuild.sh'
          }
        }
        stage('Pre2') {
          environment {
            DEVICE = 'dev2'
          }
          steps {
            build 'Demo2Job1'
          }
        }
      }
    }
    stage('Build') {
      steps {
        build 'Demo2MultiConfig'
      }
    }
    stage('Deliver') {
      parallel {
        stage('Deliver') {
          steps {
            sh 'echo done'
          }
        }
        stage('') {
          steps {
            build 'solopipeline'
          }
        }
      }
    }
  }
}