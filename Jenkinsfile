pipeline {
  agent any
  stages {
    stage('build') {
      step([$class: 'DockerComposeBuilder', dockerComposeFile: 'docker-compose.yml', option: [$class: 'StartAllServices'], useCustomDockerComposeFile: true])
      steps {
        sh 'ls -la'
      }
    }

  }
}
