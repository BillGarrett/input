pipeline {
  agent none
  stages {
    stage('Input') {
      options {
        timeout(time: 10, unit: 'SECONDS')
      }
      input {
        message 'Should we continue?'
      }
      steps {
        echo 'Where does this run?'
      }
    }
    stage('Print') {
      agent any
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