pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Ok'
        dockerNode(image: 'hello-world') {
          sh 'whoami'
        }

      }
    }

  }
  environment {
    test = 'test'
  }
}