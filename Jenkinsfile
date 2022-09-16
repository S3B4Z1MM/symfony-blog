pipeline {
  agent any
  
  stages {
    stage("build") {
      steps {
        echo 'Start building ... '
        
        sh 'ls -la' 
      }
    }
    
    stage("test") {
      steps {
        echo 'Start testing ...'
      }
    }
    
    stage("deploy") {
      steps {
        echo 'Start deolying ...'
      }
    }
  }
}
