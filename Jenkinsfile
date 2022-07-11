pipeline {
  agent {label 'mac'}
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('build') {
      steps {
        sh 'php --version'
      }
    }
  }
}