pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        git(url: 'https://github.com/Ramkhushi/know-blueocean.git', branch: 'main')
      }
    }

    stage('stage2') {
      parallel {
        stage('stage2') {
          steps {
            echo 'Hello world'
          }
        }

        stage('stage2.1') {
          steps {
            sh 'whoami'
          }
        }

      }
    }

    stage('stage3') {
      steps {
        sleep 300
      }
    }

  }
  environment {
    env = 'prd'
  }
}