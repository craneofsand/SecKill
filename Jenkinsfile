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
        sh 'mvn clean package'
        sh 'java -jar /var/lib/jenkins/workspace/SecKill_main/target/SecKill.jar &'
        sh 'echo "application is running!"'
      }
    }

    stage('Test') {
      steps {
        sh 'echo "Chech whether project works well"'
        sh 'curl http://172.19.241.93:8001/login/to_login --data "mobile=18844112403&password=123456"'
      }
    }

  }
  environment {
    CI = 'true'
  }
}
