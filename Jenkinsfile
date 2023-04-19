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
        sh "docker compose -f docker-compose.local.yml down"
        sh "docker compose -f docker-compose.local.yml up -d --build"
      }
    }
  }
}