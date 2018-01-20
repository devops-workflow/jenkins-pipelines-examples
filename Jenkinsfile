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
stage('Package App') {
  stage('Build package') {}
  stage('Publish package') {}
}
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

milestone 1

stage('Deploy Dev'){
  node('slave') {
    echo 'Deploying to Dev'
  }
}
stage('Deploy QA') {
  node('slave') {
    echo 'Deploying to QA'
  }
}
stage('Deploy Prod') {
  node('slave') {
    echo 'Deploying to prod'
  }
}
