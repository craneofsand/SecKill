pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "install running enviroment"'
      }
    }

    stage('Run') {
      steps {
        sh 'ehco "Start run application"'
      }
    }

    stage('Test') {
      steps {
        sh 'echo "Check whether project works well"'
      }
    }

  }
  environment {
    CI = 'true'
  }
}