pipeline {
  agent any
  stages {
    stage('Prebuild') {
      parallel {
        stage('Prebuild') {
          steps {
            echo 'This is pre build stage'
          }
        }

        stage('Check command in pre build stage') {
          steps {
            sh 'pwd'
          }
        }

      }
    }

    stage('Build') {
      steps {
        echo 'Builuding build'
        timeout(time: 5)
      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

    stage('Production') {
      steps {
        echo 'Production'
      }
    }

  }
}