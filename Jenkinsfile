@Library('mylib') _
pipeline {
  agent any
  environement {
    FOO = 'my message'
  }
  stages {
    stage('Test') {
      steps {
        echo 'hello world'
        sendNotifications 'SUCCESS'
        sh 'exit 1'
      }
    }
  }
  post {
    always {
      echo 'I will always say Hello again!'
      
    }
    failure {
      echo 'I will fail'
      
    }
    
  }
}
