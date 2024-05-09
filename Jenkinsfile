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
    stage {
      steps {
        sh '''
        docker rmi python
        '''
      }
    }
    }

  }
  triggers {
    pollSCM('* * * * *')
  }
}
