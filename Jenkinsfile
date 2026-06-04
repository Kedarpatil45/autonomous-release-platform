pipeline {
agent any

stages {

    stage('Hello') {
        steps {
            echo 'Autonomous Release Platform Pipeline Started'
        }
    }

    stage('Git Check') {
        steps {
            sh 'git --version'
        }
    }

    stage('Application Verification') {
        steps {
            sh 'ls -la'
            sh 'cat Dockerfile'
        }
    }

    stage('Docker Build') {
        steps {
            sh 'docker build -t flask-app:latest .'
        }
    }

}

}
