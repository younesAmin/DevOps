pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sleep 30
      }
    }

    stage('Unit Tests') {
      parallel {
        stage('Unit Tests') {
          steps {
            sleep 110
          }
        }

        stage('Junit') {
          steps {
            sleep 30
          }
        }

      }
    }

    stage('SonarQube') {
      steps {
        sleep 315
        sh 'echo \'sonar\''
      }
    }

    stage('package') {
      parallel {
        stage('package') {
          steps {
            sleep 70
          }
        }

        stage('docker build') {
          steps {
            sleep 55
          }
        }

        stage('docker test') {
          steps {
            sleep 34
          }
        }

      }
    }

    stage('Publish') {
      steps {
        sleep 240
      }
    }

    stage('Clean env') {
      steps {
        sleep 20
      }
    }

  }
}