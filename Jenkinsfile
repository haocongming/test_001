pipeline {
    agent { docker 'python:3.5.1' }
    stages {
        stage('build') {
            steps {
                bat 'python --version'
            }
        }
    }
}

node('docker') {
    checkout scm
    stage('Build') {
        docker.image('python:3.5.1').inside {
            bat 'python --version'
        }
    }
}
