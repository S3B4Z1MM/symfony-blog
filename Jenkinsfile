pipeline {
  agent {
    dockerfile {
      filename 'docker-compose.yml'
    }

  }
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
}