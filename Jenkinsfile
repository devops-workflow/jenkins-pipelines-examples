
stage('Build Docker') {
  node('slave') {
    stage('Prep') {
      echo 'Prep for build'
    }
    stage('Build') {
      echo 'Building docker image'
    }
    stage('Validate') {
      echo 'Validate docker image'
    }
    stage('Upload') {
      echo 'Upload image to registry'
    }
  }
}
milestone 1
stage('Deploy One'){
  node('slave') {
    echo 'Deploying to one'
  }
}
stage('Deploy Test') {
  node('slave') {
    echo 'Deploying to test'
  }
}
stage('Deploy Prod') {
  node('slave') {
    echo 'Deploying to prod'
  }
}
