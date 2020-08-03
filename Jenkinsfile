node {
  checkout scm
  sh "git rev-parse --short HEAD > commit-id"
  stage "Build"
    sh "cat deployment.yaml"
}
