@Library('mylib') _
pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        echo 'hello world'
        sendNotifications 'SUCCESS'
      }
    }
  }
  post {
    always {
      echo 'I will always say Hello again!'
      
    }
    
  }
  notifications {
    success {
        sh 'echo hello'
    }
  }
}
