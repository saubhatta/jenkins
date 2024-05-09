pipeline {
  agent {
    docker { image 'python:slim' }
  }
  stages {
    stage('Test') {
      steps {
        python3 hello.py
      }
    }
  }
}
