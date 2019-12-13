pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }

    stage('Software Testing') {
      parallel {
        stage('API Test') {
          environment {
            CI = 'true'
          }
          steps {
            sh 'echo \'The deployment was succesfully executed\''
          }
        }

        stage('Unit Testing') {
          steps {
            sh 'echo \'The deployment was succesfully executed\''
          }
        }

        stage('Integration Tests') {
          steps {
            sh 'echo \'The deployment was succesfully executed\''
          }
        }

      }
    }

    stage('Hardaware Testing') {
      parallel {
        stage('Sensor Test') {
          steps {
            sh 'echo \'The deployment was succesfully executed\''
          }
        }

        stage('Trigger Test') {
          steps {
            sh 'echo \'The deployment was succesfully executed\''
          }
        }

        stage('Device Control Test') {
          steps {
            sh 'echo \'The deployment was succesfully executed\''
          }
        }

      }
    }

    stage('Cloud Test') {
      steps {
        sh 'echo \'The deployment was succesfully executed\''
      }
    }

    stage('Deployment') {
      steps {
        sh 'echo \'The deployment was succesfully executed\''
      }
    }

  }
}