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

    stage('Auto Deploy') {
        steps {
            sh
            docker stop flask-container || true
            docker rm flask-container || true

            docker run -d \
              --name flask-container \
              -p 5000:5000 \
              flask-app:latest
        }
    }
}

}
