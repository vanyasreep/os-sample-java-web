pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/santosh52krishna/os-sample-java-web.git', branch: 'master', credentialsId: 'santosh52krishna')
      }
    }
    stage('Build') {
      steps {
        build 'mvn clean install'
      }
    }
  }
}