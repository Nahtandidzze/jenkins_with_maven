pipeline {
  agent {
    node {
      label 'master'
    }
  }
  environment {
    TestVariable = "testValue"
  }
  stages {
    stage('Show env') {
      steps {
        sh "printenv"
      }
    }
    stage('Build and Publish Image') {
      steps {
        sh "echo $TestVariable"
      }
    }
  }
  post {
    failure {
      echo "Build failed"
    }
  }
}
