pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/santosh52krishna/os-sample-java-web.git', branch: 'master', credentialsId: 'santosh52krishna')
      }
    }
    stage ('Build') {
            //sh "echo 'shell scripts to build project...'"
        }
    stage ('Tests') {
	parallel 'static': {
               // sh "echo 'shell scripts to run static tests...'"
            },
            'unit': {
               // sh "echo 'shell scripts to run unit tests...'"
            },
            'integration': {
               // sh "echo 'shell scripts to run integration tests...'"
            }
        }
        stage ('Deploy') {
            //sh "echo 'shell scripts to deploy to server...'"
        }
	
	
   
  }
}
