pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'su root'
                sh 'npm config set registry https://registry.npmmirror.com/'
                sh 'npm install'
            }
        }
    }
}
