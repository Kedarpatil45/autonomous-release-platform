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

    stage('Build Complete') {
        steps {
            echo 'Pipeline Successful'
        }
    }

    stage('Application Verification') {
        steps {
            sh 'ls -la'
            sh 'cat Dockerfile'
        }
    }
}

}
