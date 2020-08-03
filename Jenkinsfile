node {
  checkout scm
  sh "git rev-parse --short HEAD > commit-id"
  stage "Build"
  withKubeConfig([credentialsId: 'my_kubernetes', serverUrl: 'http://127.0.0.1:34341/']) {
      sh 'kubectl apply -f deployment.yaml'
  }
}
