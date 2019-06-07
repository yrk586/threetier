pipeline {
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        git 'https://github.com/mohanraz81/threetier'
      }
    }
    stage('Building image') {
      steps {
        script {
          def frontend = docker.build( "registry:${env.BUILD_NUMBER}", "frontend" )
        }

      }
    }
    stage('test') {
      steps {
        ansiblePlaybook 'deployment/database/createdb.yaml'
      }
    }
  }
  environment {
    registry = 'mohanraz81/candlfrontend'
    registryCredential = 'dockerhub'
  }
}