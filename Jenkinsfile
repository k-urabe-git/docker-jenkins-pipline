pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello Jenkins-pipeline'
            }
        }
        stage("ls -a") {
            steps {
                sh "ls -a"
            }
        }
        stage("pwd") {
            steps {
                sh "pwd"
            }
        }
    }
}