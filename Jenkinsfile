pipeline {
  agent {
    docker { image 'python:3.13.0b1-slim-bullseye' }
  }
  stages {
    stage('Hello') {
      steps {
        python3 hello.py
      }
    }
  }
}
