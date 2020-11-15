pipeline {
  agent any
  stages {
    stage('Build') {
      post {
        always {
          archiveArtifacts(artifacts: '*.test', fingerprint: true)

        }

        success {
          echo 'DONE!'

        }

      }
      steps {
        echo 'Placeholder'
        bat 'echo 1 > a.test'
      }
    }
    stage('Test') {
      parallel {
        stage('Test A') {
          steps {
            echo 'Testing A'
          }
        }
        stage('Test B') {
          steps {
            echo 'Testing B'
          }
        }
      }
    }
    stage('Confirm Deployment') {
      steps {
        input(message: 'Do you want to deploy?', ok: 'Go for it!', submitter: 'alex')
      }
    }
    stage('Deploy') {
      steps {
        echo 'Placeholder'
      }
    }
  }
}