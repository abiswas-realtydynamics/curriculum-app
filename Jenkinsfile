pipeline {
  agent any
  stages {
    stage('Checkout Branch') {
      steps {
        git(url: 'https://github.com/abiswas-realtydynamics/curriculum-app.git', branch: 'dev')
      }
    }

    stage('List') {
      parallel {
        stage('List') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End Unit Test') {
          steps {
            sh '''cd curriculum-front 



&& pwd && npm i && npm run test:unit'''
          }
        }

      }
    }

  }
}