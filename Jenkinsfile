pipeline {
  agent any
  stages {
    stage('Build PHP') {
      steps {
        sh 'cd symfony && composer install'
      }
    }

  }
  environment {
    test = 'test'
  }
}