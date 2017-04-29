@Library('mylib') _
pipeline {
  agent any
  environment {
    FOO = 'my message'
  }
  parameters {
     string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
  }
  stages {
    stage('Test') {
      steps {
        echo "hello world ${params.PERSON}"
        sendNotifications 'SUCCESS'
      }
    }
  }
  post {
    always {
      echo 'I will always say Hello again! :'
      
    }
    failure {
      echo 'I will fail'
      
    }
    
  }
}
