pipeline {
  agent {
    label 'jdk9'
  }
  stages {
    stage('Say hello') {
      steps {
        echo "Hello ${ENV}!"
        sh 'java -version'
      }
    }
  }
  environment {
    ENV = 'SIT'
  }
}