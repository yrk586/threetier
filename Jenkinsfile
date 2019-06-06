pipeline {
  environment {
    registry = "mohanraz81/candlfrontend"
    registryCredential = "dockerhub"
  }
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        git 'https://github.com/mohanraz81/threetier'
      }
    }
    stage('Building image') {
      steps{
        script {
          def frontend = docker.build( "registry:${env.BUILD_NUMBER}", "frontend" )
        }
      }
    }
  }
}
