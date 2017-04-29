@Library('mylib') _
pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        echo 'hello world'
        sendNotification 'SUCCESS'
      }
    }
  }
  post {
    always {
      echo 'I will always say Hello again!'
      
    }
    
  }
}
