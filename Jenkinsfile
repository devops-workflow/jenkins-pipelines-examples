stage('Static Analysis - Source') {
  parallel(
    'Lint': {},
    'Dependencies': {},
    'Security': {}
    )
}
stage ('Build App') {
  echo 'Build app'
}
stage('UnitTests') {}
stage('Analyze dockerFile') {
  parallel(
    'Static Analysis': {},
    'Compliance': {}
    )
}
stage('Build Container') {
  echo 'Build container image'
}
stage('Analyze docker image') {
  parallel(
    'Static Analysis': {},
    'Compliance': {},
    'Security': {},
    'Dependencies': {}
    )
}
stage('Test Container') {
  echo 'Run container and test'
}
stage('Publish docker image') {
  echo 'Upload to registry'
}

stage('Build Container') {
  parallel(
    'IQ-BOM': {
    },
    'Static Analysis': {
      echo '...run SonarQube or other SAST tools here'
    },
    'Build Container': {
    })
}
'Test Container'
// OLD
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
