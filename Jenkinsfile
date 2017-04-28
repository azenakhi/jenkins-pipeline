pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        echo 'hello world'
      }
    }
    stage('Install') {
      steps {
        sh '''#!/bin/bash
echo "hello world"'''
      }
    }
  }
  post {
    always {
      echo 'I will always say Hello again!'
      
    }
    
  }
}