pipeline {
  agent any
  environment {
    FOO = 'my message'
  }
  parameters {
     string(name: 'PERSON', defaultValue: 'hello', description: 'Who should I say hello to?')
     booleanParam(name: 'DEBUG_BUILD', defaultValue: true, description: '')
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
      echo "I will always say Hello again! : ${env.FOO}"
      
    }
    failure {
      echo 'I will fail'
      
    }
    
  }
}
