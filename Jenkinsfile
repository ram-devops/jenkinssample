pipeline {
  agent any
  stages {
    stage('CLONE') {
      steps {
        git(url: 'https://github.com/ram-devops/mvnrepo', branch: 'master', poll: true)
      }
    }
    stage('Maven') {
      steps {
        parallel(
          "clean": {
            sh 'mvn clean'
            
          },
          "compile": {
            sh 'mvn compile'
            
          },
          "package": {
            sh 'mvn package'
            
          }
        )
      }
    }
  }
}