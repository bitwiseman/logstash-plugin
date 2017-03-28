pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Jenkins Build of Plugin'
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Platform 1": {
            echo 'Running Test Platform 1'
            
          },
          "Platform 2": {
            echo 'Running Tests for Platform 2'
            
          },
          "Platform 3": {
            echo 'Running Tests for Platform 3'
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying to Staging Environment'
      }
    }
  }
}