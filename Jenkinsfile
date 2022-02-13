pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Install running enviroment"'
        sh 'sh install.sh'
      }
    }

    stage('Run') {
      steps {
        sh 'echo "Start application"'
      }
    }

    stage('Test') {
      steps {
        sh 'echo "Chech whether project works well"'
      }
    }

  }
  environment {
    CI = 'true'
  }
}
