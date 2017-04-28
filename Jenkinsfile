pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        parallel(
          "Test": {
            echo 'hello world'
            
          },
          "Test2": {
            git(poll: true, url: 'git@github.com:azenakhi/go-learn.git', branch: 'master')
            
          }
        )
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