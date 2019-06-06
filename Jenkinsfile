pipeline {
  agent any
  stages {
    stage('frontend') {
      parallel {
        stage('frontend') {
          steps {
            sh 'docker build -t mohanraz81/candlfrontend:"${BUILD_NUMBER}" frontend'
          }
        }
        stage('bacend') {
          steps {
            sh 'docker build -t mohanraz81/candlbackend:1.0  backend'
          }
        }
      }
    }
  }
}