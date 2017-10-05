pipeline {
  agent any
  stages {
    stage('CLONE') {
      steps {
        git(url: 'https://github.com/ram-devops/mvnrepo', branch: 'master', poll: true)
      }
    }
  }
}