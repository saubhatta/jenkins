pipeline {
  agent {
    docker {
      image 'python:alpine3.19'
    }

  }
  stages {
    stage('Hello') {
      steps {
        sh '''
        python3 hello.py
        hostname
        '''
      }
    }

  }
  triggers {
    pollSCM('* * * * *')
  }
}