pipeline {
  agent {
    docker { image 'devopsjourney1/myjenkinsagents:python' }
  }
  stages {
    stage('Hello') {
      steps {
        python3 hello.py
      }
    }
  }
}
