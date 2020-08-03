node {
  checkout scm
  sh "git rev-parse --short HEAD > commit-id"
  stage "Build"
  withKubeConfig([credentialsId: 'minikube', serverUrl: 'https://172.17.0.3:8443']) {
      sh 'kubectl apply -f deployment.yaml'
  }
}
