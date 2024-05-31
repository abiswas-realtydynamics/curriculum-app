pipeline {
  agent any
  stages {
    stage('Checkout Branch') {
      steps {
        git(url: 'https://github.com/abiswas-realtydynamics/curriculum-app.git', branch: 'dev')
      }
    }

    stage('List') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Unit Test') {
      steps {
        sh 'chmod -R 777 curriculum-front  && cd curriculum-front && pwd && npm i && npm run test:unit'
      }
    }

  }
}