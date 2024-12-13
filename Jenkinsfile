pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 --user root'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install --registry https://registry.npmmirror.com'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
