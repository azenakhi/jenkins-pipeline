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
            git(poll: true, url: 'git@github.com:azenakhi/go-learn.git', branch: 'master', credentialsId: '5d3cbd61-f5e9-4658-82fd-db4fba6c06e2')
            
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