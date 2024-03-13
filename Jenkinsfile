pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/manualchurch/jenkins1', branch: 'dev')
      }
    }

    stage('listdir') {
      parallel {
        stage('listdir') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End Unit Test') {
          steps {
            sh '''cd curriculum-front && npm -i && npm run test:unit
'''
          }
        }

      }
    }

  }
}