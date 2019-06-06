pipeline {
  agent any
  stages {
    stage('frontend') {
      steps {
        sh 'docker build -t mohanraz81/candfrontend:$BUILD_NUMBER frontend'
      }
    }
  }
}