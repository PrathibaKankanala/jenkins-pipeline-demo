pipeline {
  agent {
    label 'jdk9'
  }
  stages {
    stage('Say hello') {
      steps {
        echo "Hello ${ENV}!"
        sh 'java -version'
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
      }
    }
  }
  environment {
    ENV = 'SIT'
    TEST_USER = credentials('test-user')
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}