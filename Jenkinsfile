pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/manualchurch/jenkins1', branch: 'dev')
      }
    }

    stage('listdir') {
      steps {
        sh 'ls -la'
      }
    }

  }
}