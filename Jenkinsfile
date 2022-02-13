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
        sh 'cd src/main/java/com/imooc/miaosha'
        sh 'javac MainApplication.java'
        sh 'java MainApplication'
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