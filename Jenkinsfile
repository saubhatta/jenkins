pipeline {
  agent {
    docker { image 'devopsjourney1/myjenkinsagents:python' }
  }
  stages {
    stage('Hello') {
      steps {
        sh '''
        python3 --version
        hostname
        '''
      }
    }
  }
}
