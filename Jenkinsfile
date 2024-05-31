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

        stage('Install Node') {
          steps {
            sh 'curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash'
            sh 'exec "$SHELL"'
            sh 'nvm install 20'
          }
        }

      }
    }

    stage('Unit Test') {
      steps {
        sh 'chmod -R 777 curriculum-front && echo $(node -v) && cd curriculum-front && pwd && npm i && npm run test:unit'
      }
    }

  }
}