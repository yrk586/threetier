pipeline {
  agent any
  stages {
    stage('frontend') {
      steps {
        sh 'docker build -t mohanraz81/candlfrontend:1.0 frontend'
      }
    }
  }
}