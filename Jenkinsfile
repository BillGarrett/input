pipeline {
  agent any
  stages {
    stage('Print') {
      options {
        timeout(time: 10, unit: 'SECONDS')
      }
      input {
        message 'Should we continue?'
      }
      steps {
        sh 'echo Thank you!'
      }
    }
  }
  post {
    aborted {
      echo 'Too slow!'

    }

  }
}