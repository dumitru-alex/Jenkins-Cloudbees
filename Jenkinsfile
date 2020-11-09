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
      steps {
        bat 'echo TEST'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Placeholder'
      }
    }
  }
}