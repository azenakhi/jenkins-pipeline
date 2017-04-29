@Library('mylib') _
pipeline {
  agent any
  environment {
    FOO = 'my message'
  }
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
    failure {
      echo 'I will fail "${FOO}"'
      
    }
    
  }
}
