pipeline {
  agent any
  environment {
    DOCKERHUB_USER = "kurabedocker"
    BUILD_HOST = "root@192.168.190.130"
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
        sh "ssh://${BUILD_HOST}"
        sh "mkdir test"
        sh "docker compose up -d --build"
      }
    }
  }
}