pipeline {
  agent any
  stages {
    stage('Example') {
      steps {
        parallel(
          "Example": {
            echo 'Hello World'
            
          },
          "deploy": {
            echo 'hello world'
            
          }
        )
      }
    }
  }
  post {
    always {
      echo 'I will always say Hello again!'
      
    }
    
  }
}