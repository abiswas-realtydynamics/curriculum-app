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

    stage('') {
      steps {
        sh 'docker build -f curriculum-front/Dockerfile .'
      }
    }

  }
}