pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'PES2UG21CS929-1'
        sh 'g++ main/hello.cpp -o output'
        echo 'Build Successful!'
      }
    }
    stage('Test') {
      steps {
        sh './output'
        echo 'Test Successful!'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Successfully deployed!'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline Failed!'
    }
  }
}
