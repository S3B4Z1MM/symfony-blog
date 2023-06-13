pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'cd symfony && composer install'
      }
    }

  }
  environment {
    test = 'test'
  }
}