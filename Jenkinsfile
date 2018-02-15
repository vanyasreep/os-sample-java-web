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
        sh 'echo Build'
      }
    }
    stage('Test') {
      steps {
        sh '''parallel (
        "JUnit": { 
            sh "echo JUnit"
        },
        "DBUnit": { 
            sh "echo DBUnit"
        },
        "Jasmine": { 
            sh "echo Jasmine"
        },
      )'''
        }
      }
      stage('Dev') {
        steps {
          sh 'sh "echo Dev"'
        }
      }
      stage('Staging') {
        steps {
          sh 'sh "echo Staging"'
        }
      }
      stage('Production') {
        steps {
          sh ' sh "echo Production"'
        }
      }
    }
  }