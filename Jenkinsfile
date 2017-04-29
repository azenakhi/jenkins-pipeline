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
        echo 'hello world'
        sendNotifications 'SUCCESS'
      }
    }
  }
  post {
    always {
      echo 'I will always say Hello again! : '${FOO}
      
    }
    failure {
      echo 'I will fail'
      
    }
    
  }
}
