pipeline {
  agent { node { label 'slave' } }
  stages {
    stage('Build') {
      steps {
        echo 'Build'
      }
    }
    stage('Parallel Testing') {
      parallel {
        stage('Test 1') {
          agent { label 'slave'}
          steps { echo 'Test 1'}
        }
        stage('Test 2') {
          agent { label 'slave'}
          steps { echo 'Test 2'}
        }
        stage('Test 3') {
          agent { label 'slave'}
          steps { echo 'Test 3'}
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
  post {
    always {
      echo 'Done'
    }
  }
}
