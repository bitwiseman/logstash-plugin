node('') {
  parallel(
    "Platform 4": {
      parallel(
        "Platform 4.1": {
          echo 'Running Test Platform 1'
        },
        "Platform 4.2": {
          echo 'Running Test Platform 1'
        }
      )
    },
    "Platform 5": {
      parallel(
        "Platform 5.1": {
          echo 'Running Test Platform 1'
        },
        "Platform 5.2": {
          echo 'Running Test Platform 1'
        }
      )
    }
  )
  stage('Build') {
      echo 'Jenkins Build of Plugin'
  }
  stage('Test') {
    parallel(
      "Platform 1": {
        stage('Test3') {
          echo 'Running Test Platform 1'
        }
      },
      "Platform 2": {
        echo 'Running Tests for Platform 2'

      },
      "Platform 3": {
        echo 'Running Tests for Platform 3'

      }
    )
  }
  stage('Deploy') {
    parallel(
      "Target 1": {
        echo 'Deploying to Staging Environment'

      },
      "Target 2": {
        echo 'Target 2'

      }
    )
  }
}
