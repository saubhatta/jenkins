pipeline {
  agent none
  stages {
    stage('Hello') {
      agent {
        docker {
          image 'python:alpine3.19'
        }
      }
      steps {
        sh 'echo $BUILD_NUMBER'
        sh '''
        python3 hello.py
        hostname
        '''
      }
    }
    stage('Cleanup') {
      agent any
      steps {
        sh '''
        docker rmi python:alpine3.19
        '''
      }
    }
  }
  triggers {
    pollSCM('* * * * *')
  }
}
