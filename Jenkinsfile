pipeline {
  environment {
    registry = "badsanni/test"
    registryCredential = 'DH_ID'
  }
  agent any
  stages {
    stage('Cloning Git') {
      steps {
        git 'https://github.com/badsanni/jenkins.git'
      }
    }
    stage('Building image') {
      steps{
        script {
          docker.build registry + ":$BUILD_NUMBER"
        }
      }
    }
  }
}
