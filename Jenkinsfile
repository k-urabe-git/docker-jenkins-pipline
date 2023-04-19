pipeline {
  agent any
  environment {
    DOCKERHUB_USER = "kurabedocker"
  }
  stages {
    stage('Pre Check') {
      steps {
        sh "test -f ~/.docker/config.json"
        sh "cat ~/.docker/config.json | grep docker.io"
      }
    }
    stage('Build') {
      steps {
        sh "docker compose up -d --build"
      }
    }
  }
}