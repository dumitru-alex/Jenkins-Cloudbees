pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Placeholder'
        bat 'echo 1 > a.test'
        archiveArtifacts(artifacts: '*.test', fingerprint: true)
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
    stage('Deploy') {
      steps {
        echo 'Placeholder'
      }
    }
  }
}